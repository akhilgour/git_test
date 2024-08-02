FROM python:3
WORKDIR /code
ENV FLASK_APP=test.py
ENV FLASK_RUN_HOST=-vm166-172.mip.storage.hpecorp.net
COPY req.txt req.txt
RUN pip install --proxy http://hpeproxy.its.hpecorp.net:80 -r req.txt  
EXPOSE 5001
COPY . .
CMD ["flask", "run", "--debug"]
