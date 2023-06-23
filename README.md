# Django_Feedback_Form
#With Celery task management
from celery import Celery

app = Celery('hello', broker='amqp://guest@localhost//')

@app.task
def reverse(text):
    return text[::-1]
print(reverse('Hello'))

Ouput:
olleH

Process finished with exit code 0
     
