# TicketsPlus

## Project Setup

This is an event ticket sales webapp that allows users to manage venues, concerts, concert categories, and tickets.

Its database has the following entity-relationship model:

![Tickets ER Model](https://i.ibb.co/3cLbMTD/tickets-er-model.png)


First, grab the source code from the [repository](https://github.com/yossilevi94/ticketsplus/) on GitHub:

```sh
$ git clone git@github.com:yossilevi94/ticketsplus.git 
$ cd ticketsplus
```

Create a virtual environment and activate it:

```sh
$ python3.11 -m venv env && source env/bin/activate
```

Install the requirements and migrate the database:

```sh
(venv)$ pip install -r requirements.txt
(venv)$ python manage.py migrate
```

Create a superuser and populate the database:

```sh
(venv)$ python manage.py createsuperuser
(venv)$ python manage.py populate_db
```

Run the development server:

```sh
(venv)$ python manage.py runserver
```

Open your favorite web browser and navigate to [http://localhost:8000/admin](http://localhost:8000/admin). Try using your superuser credentials to access the Django admin site

If everything goes well you should get the `Successfully populated the database` message. Start the development server (if it isn't running already) and navigate to your admin dashboard once again. Then check if the database was populated with some venues, concert categories, concerts, and tickets.

![Django Admin Interface Theme Customization](https://i.ibb.co/jLQmCBf/django-admin-interface-customization.png)

## Conclusion
