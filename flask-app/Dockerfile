FROM python:3.9-buster

# set a directory for the app
WORKDIR /usr/src/app

ENV VIRTUAL_ENV=/opt/venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"



# copy all the files to the container
COPY . .

# install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# expose port 5000 for running the app
EXPOSE 5000

# run the command for launching the app
CMD ["python3", "./app.py"]

