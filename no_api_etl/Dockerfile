FROM python:3.6

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN svn export --force https://github.com/LCBRU/no_api_etl/trunk/ /usr/src/app/

RUN pip install --no-cache-dir -r requirements.txt

CMD [ "python", "-u", "/usr/src/app/uhl_etl.py" ]