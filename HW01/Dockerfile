# Fill in this file with the Dockerfile instructions as described in the README.md

# NOTE: When filling in this file, assume this file is located inside the
# toyota-data-feeder directory like following:

#        toyota-data-feeder/
#        ├── Dockerfile
#        ├── ca.crt
#        ├── feeder.py
#        ├── readme.md
#        ├── requirements.txt
#        ├── toyota_data.csv
#        └── assets
FROM python:3.12-slim

WORKDIR /app

RUN pip install --no-cache-dir paho-mqtt==1.6.1

COPY feeder.py toyota_data.csv ca.crt ./

ENV PYTHONUNBUFFERED=1

CMD ["python", "feeder.py"]