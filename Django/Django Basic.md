- **manage.py** does the same thing as **django-admin** but also sets the DJANGO_SETTINGS_MODULE environment variable so that it points to the project’s settings.py file.
- django-admin is Django’s command-line utility for administrative tasks.
- Table names are automatically generated by combining the name of the app (`polls`) and the lowercase name of the model – `question` and `choice`.
- The reason that there are separate commands to make and apply migrations is because you’ll commit migrations to your version control system and ship them with your app; they not only make your development easier, they’re also usable by other developers and in production.
- The template system uses dot-lookup syntax to access variable attributes.
- request.POST is a dictionary-like object that lets you access submitted data by key name.
- Always return an HttpResponseRedirect after successfully dealing with POST data. This prevents data from being posted twice if a user hits the Back button.
- Each generic view needs to know what model it will be acting upon. This is provided using the model attribute.
- The DetailView generic view expects the primary key value captured from the URL to be called "pk".
- 