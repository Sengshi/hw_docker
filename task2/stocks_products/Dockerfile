FROM python:3.11

COPY . /src

WORKDIR /src

RUN pip3 install --no-cache-dir --upgrade -r requirements.txt

ENV S_KEY='django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j' \
    DJ_DEBUG='False'


EXPOSE 8080

RUN ["python3", "manage.py", "makemigrations"]
RUN ["python3", "manage.py", "migrate"]

CMD ["python3", "manage.py", "runserver", "0.0.0.0:8080"]
