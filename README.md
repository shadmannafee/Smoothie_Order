# Smoothie_Order
#This is a code for making payment receipt for orders in the Smoothie Shop.
cost = 0
user = input('Press any key to order -')
print('''
Welcome to Smooth Smoothies Smoothie Ordering System

Which smoothie would you like?
1) $ 4.99 Pineapple Banana
2) $ 6.49 Almond Basil
3) $ 0.99 Purple Surprise
4) $ 9.99 Onion Toffee''')

smoothie_type = int(input('Your choice (1-4): '))

if smoothie_type == 1:
    cost+= 4.99
elif smoothie_type == 2:
    cost+= 6.49
elif smoothie_type == 3:
    cost+= 0.99
elif smoothie_type == 4:
    cost+= 9.99
    
print('''
Which size would you like?
1) $ -2.0 small
2) $ 0.0 medium
3) $ 2.0 large
4) $ 100.0 galactic''')

smoothie_size = int(input('Your choice (1-4): '))

if smoothie_size == 1:
    cost-=2.0
elif smoothie_size == 2:
    cost+= 0
elif smoothie_size == 3:
    cost+= 2.0
elif smoothie_size == 4:
    cost+= 100.0
    
print('''
Which topping would you like?
1) $ 0.0 no topping
2) $ 1.0 cinnamon
3) $ 1.0 chocolate shavings
4) $ 1.0 shredded coconut''')
toppings = int(input('Your choice (1-4): '))
if toppings == 1:
    cost-= 0.0
elif toppings == 2:
    cost+= 1.0
elif toppings == 3:
    cost+= 1.0
elif toppings == 4:
    cost+= 1.0
    
#print('Sub-total- $',cost)

vat = 0.15*cost
#print('vat- $',vat)

total = vat+cost
#print('total- $',total)

final = 'You have ordered a '
if smoothie_size == 1:
    final+='small '
elif smoothie_size == 2:
    final+='medium '  
elif smoothie_size == 3:
    final+='large '
elif smoothie_size == 4:
    final+='galactic '

if smoothie_type == 1:
    final+='Pineapple Banana with '
elif smoothie_type == 2:
    final+='Almond Basil with '  
elif smoothie_type == 3:
    final+='Purple Surprise with '
elif smoothie_type == 4:
    final+='Onion Toffee with '    
    
if toppings == 1:
    final+='no toppings.'
elif toppings == 2:
    final+='cinnamon.'  
elif toppings == 3:
    final+='chocolate shavings.'
elif toppings == 4:
    final+='shredded coconut.'   
    
print(final)

print('Sub-total- $',cost)


print('vat- $',vat)


print('total- $',total)
