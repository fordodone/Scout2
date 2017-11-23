# Dockerfile
FROM python:2.7

COPY . /app

WORKDIR /app

RUN pip install -r requirements.txt \
      && python setup.py install \
      && mkdir -p /app/scout2-report

CMD [ "bash", "-c", "Scout2 --force --no-browser && mv /app/scout2-report/report.html /app/scout2-report/index.html" ]

