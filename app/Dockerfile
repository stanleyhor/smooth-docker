# our base image
FROM python:3.6-alpine

# install Python modules needed by the Python app
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

# copy files required for the app to run
COPY app.py /usr/src/app/
COPY templates /usr/src/app/templates/

# tell the port number the container should expose
EXPOSE 9000

# run the application
CMD ["python", "/usr/src/app/app.py"]
