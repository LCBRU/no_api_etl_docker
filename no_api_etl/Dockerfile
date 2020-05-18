FROM python:3.6

RUN apt-get update && \
    apt-get -y upgrade && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install mysql-client vim && \
    apt-get clean

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN echo "2010-05-18 A"

RUN svn export --force https://github.com/LCBRU/no_api_etl/trunk/ /usr/src/app/

RUN pip install --no-cache-dir -r requirements.txt

CMD [ "python", "-u", "/usr/src/app/uhl_etl.py" ]