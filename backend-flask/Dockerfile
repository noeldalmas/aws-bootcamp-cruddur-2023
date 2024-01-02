FROM python:3.10-slim-buster

# Container
WORKDIR /backend-flask

# Outside container --> inside container
COPY requirements.txt requirements.txt

# Inside container
# Install the python librariea used for the app
RUN pip3 install -r requirements.txt

# Outside container --> Inside container
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]