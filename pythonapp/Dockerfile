FROM python:3.9-alpine
LABEL Author="Dileep"
RUN apk add git && git clone https://github.com/khajasampleapps/basicflask.git
EXPOSE 8000
WORKDIR /basicflask
RUN pip install -r requirements.txt
CMD ["python3", "app.py"]
