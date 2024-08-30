FROM python
WORKDIR /app
COPY ./requirements.txt /app
RUN pip3 install -r requirements.txt
COPY . /app
EXPOSE 5000
ENV FLASK_APP=my_flask.py
CMD ["flask", "run", "--host=0.0.0.0"]

