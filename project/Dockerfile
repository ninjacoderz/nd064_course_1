FROM python:3.8
LABEL maintainer="BinhNT"

COPY . /app
WORKDIR /app
RUN pip install -U pip wheel setuptools && \
    pip install -r requirements.txt
RUN python init_db.py

EXPOSE 3111

# command to run on container start
CMD [ "python", "app.py" ]