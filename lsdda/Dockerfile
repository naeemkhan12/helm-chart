FROM python:3.5.5-slim-jessie
RUN apt-get update && apt-get install -y git --no-install-recommends
COPY . /src
ENV FLASK_APP=app.py
RUN cd /src/flask-mongo-starter\
&& pip install -r requirements.txt
WORKDIR /src/flask-mongo-starter/app
EXPOSE 5000
ENTRYPOINT [ "flask" ]
CMD [ "run","--host=0.0.0.0" ]
