FROM python:3.8

ENV PYTHONUNBUFFERED 1

COPY pip.conf /root/.pip/pip.conf

WORKDIR /var/www/html/backend

ADD . /var/www/html/backend

RUN /usr/local/bin/python -m pip install --upgrade pip \
&& pip install -r requirements.txt \
&& sed -i 's/\r//' ./start.sh \
&& chmod +x ./start.sh
