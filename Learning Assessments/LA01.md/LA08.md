```python
              DELETE
class Book:
    def init(self,title,author):
        self.title = title
        self.author = author

buk1 = Book("Isang Kaibigan", "Sarah Duterte")
print(buk1.title, buk1.author)
del buk1.author
buk2 = Book("The hunger Games", "Suzanne Collins")
print(buk1.title, buk1.author)
print(buk2.title, buk2.author)
```python
