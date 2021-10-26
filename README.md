# Deploy_To_Heroku
--------------------

# Heroku Deployment Common Problems I Faced:-

---------------------------------------

> 1. point1:-make sure that ALLOWED_HOST=["*"] or you can also set as ["Your heroku link without https and trailing slash","localhost/127.0.0.1"]:-Otherwise disallowed Host	
> 2. Make Sure that Profile there is a Gap between web hook i.e.. web: <gunicorn /waitress/uwsgi services>:-Otherwise end up getting the H14 Error	![image-20211026142549006](C:\Users\611903295\AppData\Roaming\Typora\typora-user-images\image-20211026142549006.png)


> If you do not mention the STATIC_ROOT while declaring the static path then also get asset error
> how to check the logs is "heroku logs --app <your application name>"
> You can also disable the collect static by "heroku config :set delete_COLLECTSTATIC=1"


>Make Sure to commit All the changes in GIT as 
>git add .
>git commit -am "<any comment>"
>to push to heroku git push heroku master (But Make Sure your git remote been added to heroku by "heroku git:remote -a <Your Heroku App Name>")

# Another Way to Deploy after preparing All the changes in the been done

- ----------------------------------------------------------------------------------------

- Instead of choosing setting for the local repo we can select deploy on the github remote repo
- and we can built it by choosing the deploy option from heroku GUI dashboard and select the repo which is already added to the Git file 
- 'Check the Activity log and Log Files to see its been built properly or not'

# How to add inbuilt Postgresql Hosted on AWS EC2 instance  By Using Heroku

- for this we have to got to the resources tab and go to the setting to check the credetional
- we need to put the credetional in our settings.py file in order to Run it 
- we can migrate the postgres SQL Normally by python manage.py makemigrations and migrate 
- or we can also run heroku run python manage.py makemigrations and migrate command 
- by remember that it need the psycopg2 for running the postgresql like mysql connector for the mysql db 

 ## Heroku By Pratik:-
  -----------------------
  
   https://rocky-reef-79151.herokuapp.com/ :-Heroku With Static File Using AWS S3 Bucket and GUNICORN
  
  [](https://pratikheroku675.herokuapp.com/ :-Heroku By Using waitesss and whiteNoise
