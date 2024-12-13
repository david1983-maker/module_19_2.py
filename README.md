from task1.models import Buyer
from task1.models import Game
Buyer.objects.create(name='David', balance=120, age='35')
Buyer.objects.create(name='Mark', balance=500, age='40')
Buyer.objects.create(name='Artur', balance=70, age='17')
Game.objects.create(title='Mortal Kombat', cost=50, size=70, description='Fighting', age_limited=True) 
Game.objects.create(title='Killzone', cost=60, size=100, description='FPS', age_limited=True) 
Game.objects.create(title='Final Fantasy', cost=50, size=40, description='JRPG') 
third_buyer = Buyer.objects.get(age__lte=18)
second_buyer, first_buyer = Buyer.objects.filter(age__gt=18)
Game.objects.get(id=1).buyer.set((first_buyer, second_buyer))
Game.objects.get(id=1).buyer.set((first_buyer,second_buyer))
Game.objects.get(id=3).buyer.set((second_buyer,third_buyer)) 
