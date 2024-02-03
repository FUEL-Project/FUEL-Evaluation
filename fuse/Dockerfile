FROM python:2

RUN apt update -y && apt install -y git vim less rabbitmq-server

RUN git clone https://github.com/WSP-LAB/FUSE /fuse/
WORKDIR /fuse/
RUN pip2 install -r requirements.txt

CMD bash -c 'rabbitmq-server &; while true; do sleep 1; done'
