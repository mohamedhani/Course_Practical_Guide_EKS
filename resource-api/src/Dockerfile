FROM python:3.6.15-slim-buster
ADD requirements.txt requirements.txt
RUN pip install -r requirements.txt
RUN apt install curl -y
ADD . /
CMD [ "gunicorn", "--worker-tmp-dir", "/dev/shm", "--bind", "0.0.0.0:5000", "wsgi:app" ]