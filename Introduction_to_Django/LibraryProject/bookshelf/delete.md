### ❌ Delete Operation - Removing a Book

1. Open Django shell:
```bash
python manage.py shell


# Delete Duplicate Book Records

### Code to remove duplicates of '1984' by George Orwell

```python
from bookshelf.models import Book

duplicates = Book.objects.filter(title="1984", author="George Orwell", publication_year=1949)

# Keep the first one, delete the rest
if duplicates.count() > 1:
    for book in duplicates[1:]:
        book.delete()
```

### Output:

Deleted all duplicate books with title "1984", keeping only the first one.
