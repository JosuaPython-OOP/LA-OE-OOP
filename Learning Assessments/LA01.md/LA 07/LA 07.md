```python
                   UPDATE
class Car:
    def __init__(self,brand,color):
        self.brand = brand
        self.color = color
        
Toyota = Car("Toyota", "Red")
Toyota.color = "yellow"
Toyota.brand = "Toyota"
print(Toyota.brand, Toyota.color)

Lamborghini = Car("Lamborghini","blue")
print(Lamborghini.brand, Lamborghini.color)
```python
