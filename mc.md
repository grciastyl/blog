Mini challenge #1

1 Create a new app called 'posts'
2 create a 'urls.py' inside of posts and add the includes the urls.py in config folder (remember to add a new name for the new endpoints inside of config.urls e.g. "posts/")
3 create a new folder called posts inside of templates
    create a new file for list.html
    create a new file for detail.html
    create a new file for new.html
    create a mew file for delete.html


Mini challenge #2
1 create a new model called Post inside of models.py (in posts app)
2 The class should be inhereted from models.Model (make sure to do the right imports)
3 The attributes for this class are:
    -title is a CharField with a max length of 128
    -subtitle is a CharField with a max length of 256
    -body is a TextField
    -created_on is a DateTimeField that should auto add itself
    -author is a ForeignKey
4 Implement the methods for __str__(self) and get_absolute_url(self)
    __str__ should return the title only

Notes:
For the author field, you will use this:
author = models.ForeignKey(
    get_user_model(),
    on_delete = models.CASCADE
)


The get_user_model() you eill get it from: from django.contrib.auth import get_user_model


# Mini Challenge 3 - PostCreateView
STR:
1. Inside of posts/views.py create the class PostCreateView that inherits from CreateView (the generic class)
2. Remember to fill the following attributes: {template_name, fields, model}
3. On fields I only want to display the: title, subtitle, body and status
4. Create the url that's going to handle that view
5. Add the form into the templates/posts/new.html and make it crispy!
5. 1. Don't forget about csrf security
6. Add a new li inside of the navbar.html

