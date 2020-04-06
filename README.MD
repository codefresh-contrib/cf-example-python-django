# Deploy to Heroku Using Codefresh

![heroku and codefresh](heroku-and-codefresh.png)

This is an example Python application that uses Django, pip and Docker.

More details can be found in [the documentation page](https://codefresh.io/docs//docs/yaml-examples/examples/deploy-to-heroku/).

## Instructions

To install dependencies 

```
pip install -r requirements.txt 
```

## To run tests

```
python -m unittest composeexample.utils
```

## To run the webapp manually

```
python manage.py runserver 0.0.0.0:8000
```

....and navigate your browser to  http://localhost:8000/

## To create a docker image

```
docker build -t django-app .
```


## To run the docker image

```
docker run -p 8000:8000 django-app
```


## To use this project in Codefresh 

There are two options of deploying to Heroku with this example:

- [Deploy source code to Heroku using the heroku-deployer plugin](codefresh.yml))
- [Deploy a Docker image to Heroku using a push step](codefresh-heroku-push-image.yml)

Copy and paste your desired yaml into the in-line editor to see them in action.








