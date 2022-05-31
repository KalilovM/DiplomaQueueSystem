# Django 
***
###### В этом документе описано то как получилось реализовать функционал сайта Legacy.
***
### Используемые ресурсы
`Django` -  свободный фреймворк для веб-приложений на языке Python.
***
### Создание функционала
###### 1. Регистрация и вход пользователя
Сайт должен был иметь возможность регистрации и входа для работы с пользователями, для этого была создана система регистрации:
```
def register(request):

if request.method == 'POST':
form = UserRegistrationForm(request.POST)

if form.is_valid():
form.save()

messages.success(request, f'Your account has been created. You can log in now!')

return redirect('login')

else:
form = UserRegistrationForm()
context = {'form': form}
return render(request, 'register.html', context)

```
***
###### 2. Создание тикетов
Сайт должен был иметь возможность создания талонов ведь на них основана вся идея с электронной очередью, для этого была создана система создания талонов:
```
class TalonForm(forms.ModelForm):
class Meta:
model = Talon

fields = ('number', 'bank', 'filial','service','arriveTime')
widgets = {'arriveTime': forms.Select(choices=HOUR_CHOICES)}

  

def __init__(self, *args, **kwargs):
super().__init__(*args, **kwargs)
self.fields['filial'].queryset = Filial.objects.none()

  

if 'bank' in self.data:
try:
bank_id = int(self.data.get('bank'))

self.fields['filial'].queryset = Filial.objects.filter(bank_id=bank_id).order_by('name')

except (ValueError, TypeError):
pass # invalid input from the client; ignore and fallback to empty City queryset

elif self.instance.pk:
self.fields['filial'].queryset = self.instance.bank.filial_set.order_by('name')

```
***
###### 3. Изменение тикетов
Сайт должен был иметь возможность изменения талонов для удобства пользователей, для этого была создана система изменения талонов: 
```
class TalonUpdateView(UpdateView):

model = Talon

form_class = TalonForm

template_name = 'talon_form.html'

success_url = reverse_lazy('talon_changelist')

```
***
###### 4. Удаление тикетов
Сайт должен был иметь возможность удаления талонов для удобства пользователей, для этого была создана система удаления талонов: 
```
class TalonDeleteView(DeleteView):

model = Talon

template_name = 'talon_confirm_delete.html'

success_url = reverse_lazy('talon_changelist')

```
***
###### 5. Отображение тикетов
Сайт должен был иметь возможность отображения талонов для удобства во время использования электронной очереди, для этого была создана система динамического изменения и отображения талонов:
```
def home(request):

act = Talon.objects.filter(status='Active')

for i in act:
Talon.update_status(i)

psd = Talon.objects.filter(status='Passed')
msd = Talon.objects.filter(status='Missed')

context = {
'act' : act,
'psd' : psd,
'msd' : msd
}

return render(request, 'test.html', context)

```

```
class Talon(models.Model):
STATUS = (
('Active','Active'),
('Passed','Passed'),
('Missed','Missed')
)

user = models.ForeignKey('accounts.NewUser', on_delete=models.CASCADE)
number = models.CharField(max_length=100)
bank = models.ForeignKey(Bank, on_delete=models.CASCADE)
filial = models.ForeignKey(Filial, on_delete=models.CASCADE)
service = models.ForeignKey(Service, on_delete=models.CASCADE)
arriveTime = models.TimeField(default=dt.time(00, 00), unique=True)

status = models.CharField(max_length=64, choices=STATUS,default='Active')

```
***
###### 6. Изменение профиля
Для пользователя может оказатся важной возможность редактировать свой профиль, для этого была создана система редактирования профиля:
```
def UpdateUser(request, pk):
user = NewUser.objects.get(pk=pk)

form = UserRegistrationForm(instance=user)

if request.method == 'POST':
form = UserRegistrationForm(data = request.POST, files = request.FILES, instance=user)

if form.is_valid():
form.save()

context = {
'form' : form
}

return render(request,'user.html', context)

```
