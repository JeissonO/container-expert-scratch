FROM python:3.7-alpine

WORKDIR /app

COPY requirements.txt /app 

RUN pip3 install -r requirements.txt

COPY . /app
EXPOSE 8080
ENTRYPOINT ["python3", "app.py"]


# sudo docker build -t "mypythonapp:v1.0" .
# sudo docker run -it --name mypythonapp mypythonapp:v1.0
# sudo docker run --rm -it --name mypythonapp mypythonapp:v1.0
# sudo docker run --rm -it -p 8080:8080 -p 9090:8080 --name mypythonapp mypythonapp:v1.0