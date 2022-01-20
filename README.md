# ToDoListUsingDjango
## Title:
ToDo application with authentication using Django
## Installation

PyPI
```bash 
pip install django
pip install psycopg2
pip install jwt
```
or from source
```bash
django - https://docs.djangoproject.com/en/4.0/
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
```register page:```
![image](https://user-images.githubusercontent.com/75968886/150379365-2b4768bf-742c-43ae-8ae5-22f2dce238b0.png)
```login page:```
![image](https://user-images.githubusercontent.com/75968886/150380141-f70ebde8-6989-4de0-b109-c8275cdb2570.png)
```before adding task:```
![image](https://user-images.githubusercontent.com/75968886/150380315-be435637-ffd9-4fee-acc8-d2534f9fb9d6.png)
```adding task:```
![image](https://user-images.githubusercontent.com/75968886/150380364-e7e71ee6-2e82-431a-aa74-b2f2ec6a46cb.png)
```after adding task:```
![image](https://user-images.githubusercontent.com/75968886/150380841-884b9944-0c55-411c-8978-a8c73c37ed76.png)
Our tokens saved in database
## License
[MIT](https://choosealicense.com/licenses/mit/)
