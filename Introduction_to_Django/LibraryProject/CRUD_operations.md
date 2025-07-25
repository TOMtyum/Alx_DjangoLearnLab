# CRUD Operations in Django Shell

##  Create
```python
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

<Book: 1984>

##  retrieve

books = Book.objects.all()
for book in books:
    print(book.title, "-", book.author, "-", book.publication_year)

OUTPUT
1984 - George Orwell - 1949

UPDATE
book = Book.objects.get(title="1984")
book.title = "Nineteen Eighty-Four"
book.save()

OUTPUT
>>> book.title
'Nineteen Eighty-Four'

DELETE
book = Book.objects.get(title="Nineteen Eighty-Four")
book.delete()

OUTPUT
(1, {'bookshelf.Book': 1})

