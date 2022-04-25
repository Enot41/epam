FROM python:3.7.13-slim
WORKDIR /backend
COPY /lib_catalog .
RUN pip3 install -r requirements.txt
ENV POSTGRES_PASSWORD $POSTGRES_PASSWORD
ENV HOST $HOST
CMD ["./entrypoint.sh"] 
