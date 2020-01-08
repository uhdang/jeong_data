# TODO

- separate base, local, and production
- nginx
- postgres
- webpack
- AWS Deployment

# Run frontend, backend, and database
## Docker Compose up
$ docker-compose up --build                        # rebuild the image and activate

## database schema migrate
$ docker exec -it [CONTAINER NAME/ID] bash
$ python manage.py migrate

## Admin setup
(optional) $ python manage.py createsuperuser

## Data Check
$ docker exec -it [CONTAINER NAME of DB] bash
$ psql -U postgres




# Virtual Environment

## Using virtualenv
* cd into `jeong_backend`

```python
virtualenv -p /usr/bin/python3.6 venv       # Create a virtual environment
source venv/bin/activate                    # Activate virtual environment
deactivate                                  # Deactivate virtual environment

pip3 install -r requirements.txt            # Install packages listed in requirements.txt
```

## Using Anaconda
1. Install Anaconda
2. Create (and activate) a virtual environment for the project
```
$ conda env list                                # check available virtual environment list
$ conda create --name weview python=3.6
$ source activate weview
$ conda deactivate                              # get out of environment
```
3. Install / check packages from requirements.txt 
```
$ pip install -r requirements.txt 
$ conda list
```


# Run a postgres docker locally
```
$ docker run -p 5432:5432 --name db -e POSTGRES_PASSWORD=postgres -d postgres
```

# Django Superuser
username: root
password: dkssudwjddndi


# Mock Data

User
- user_01 :: usernumberone


# VPC url

http://ec2-3-120-139-66.eu-central-1.compute.amazonaws.com/


# NOTE on updating api

always remember to migrate updated model
```python
python3 manage.py makemigrations [app name]
python3 manage.py migrate [app name]]
```
