Manga, a sweet MongoDB abstraction layer
========================================

**note** This repo is created from package https://pypi.python.org/pypi/manga/0.1.2 who's
link to github is currently empty. This is not my work and I claim no credit for it.

Manga provides a simpler way for working with a MongoDB database.
It is provided in a single python source file with no dependencies other than
the Python Standard Library.

License: MIT (see LICENSE)

Installation and Dependencies
-----------------------------

Install bottle with ``pip install manga`` or just download manga.py and place
it in your project directory. There are no (hard) dependencies other than the
Python Standard Library.

Example
-------

.. code-block:: python

    from manga import model

    class User(Model):
        name = StringField(length=(2, 10))
        email = EmailField(required=True)

    bob = User({'name': 'Bob', 'email': 'bobby@tables.com'})
    bob.save()
