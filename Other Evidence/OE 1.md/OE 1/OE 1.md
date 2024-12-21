```python
class Mlbb_hero():
    def __init__(self, name, role, dmg_type):
        self.name = name
        self.role = role
        self.dmg_type = dmg_type
    
    def __str__(self):
        return f"{self.name} is a/an {self.role} with a {self.dmg_type} power."
    
    def describe(self):
        return self
    
mm = Mlbb_hero("Layla", "Marksman", "Physical")
mage = Mlbb_hero("Kagura", "Mage", "Magic")
jungler = Mlbb_hero("Gusion", "Jungler", "Magic")
tank = Mlbb_hero("Lolita", "Tank", "Physical")
support = Mlbb_hero("Diggies", "Support", "Magic")

print(f'''
MY TEAM:
{mm.name}
{mm.role}
{mm.dmg_type}
{mm.describe()}

{mage.name}
{mage.role}
{mage.dmg_type}
{mage.describe()}

{jungler.name}
{jungler.role}
{jungler.dmg_type}
{jungler.describe()}

{tank.name}
{tank.role}
{tank.dmg_type}
{tank.describe()}

{support.name}
{support.role}
{support.dmg_type}
{support.describe()}
""")
```python
