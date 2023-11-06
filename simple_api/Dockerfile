FROM python:2.7-buster AS builder

LABEL maintainer="feavfeav@gmail.com"

#Installer les packages
RUN apt update -y && apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y

#Installer les modules pythons
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0

#Copier les sources
COPY ./student_age.* /data/

EXPOSE 5000

CMD ["python","student_age.py"]