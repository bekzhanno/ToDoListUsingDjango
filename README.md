# ToDoListUsingDjango
## Title:
a ToDo application with authentication using Django
## Installation

PyPI
```bash 
pip install django
pip install psycopg2
pip install jwt
```
or from source
```bashdjango - https://docs.djangoproject.com/en/4.0/
psycopg2 - https://www.psycopg.org/docs/
```
## Usage
```bash
urlpatterns = [
    path('login/', CustomLoginView.as_view(), name='login'),
    path('logout/', LogoutView.as_view(next_page='login'), name='logout'),
    path('register/', RegisterPage.as_view(), name='register'),

    path('', TaskList.as_view(), name='tasks'),
    path('task/<int:pk>/', TaskDetail.as_view(), name='task'),
    path('task-create/', TaskCreate.as_view(), name='task-create'),
    path('task-update/<int:pk>/', TaskUpdate.as_view(), name='task-update'),
    path('task-delete/<int:pk>/', DeleteView.as_view(), name='task-delete'),
    path('task-reorder/', TaskReorder.as_view(), name='task-reorder'),
]
```
## Examples
Outputs will be like these:
![alt text](http://url/to/img.png)
```bash
```
Our tokens saved in database
## License
[MIT](https://choosealicense.com/licenses/mit/)
