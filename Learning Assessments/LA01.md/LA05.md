```python
class MLHero():
    def __init__(self, name, role):
        self.name = name
        self.role = role

    def describe(self):
        print(f"{self.name} is a/an {self.role} hero.")

mage = MLHero("Kagura", "Mage")
marksman = MLHero("Lesley", "Marksman")

mage.describe()
marksman.describe()
```python
