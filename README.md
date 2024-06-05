# django-to-do-app

### Cloning the repository

Clone the repository:
```
https://github.com/codeboylal/hbl3-django-project.git
```

Move into the directory: 
```
cd hbl3-django-project
```

Creating, activating a virtual environment and installing dependencies:
```
python3 -m venv env

source ./env/bin/activate

pip install -r requirements.txt
```

### Running the application
To run the application:
```
python manage.py runserver
```

Open your web browser and go to the address: http://127.0.0.1:8000/

### To Containerize Application With Docker
Create a Dockerfile:
```
FROM python:3.9

WORKDIR /

COPY . .

RUN pip install -r requirements.txt

EXPOSE 8000

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000"]

```
### Build Docker Images List and Run Container
List Docker Images:
```
docker build -t my-django-site .
docker images 
docker ps
docker run -d -p 8000:8000 my-django-site

Access website: http://127.0.0.1:8000
```