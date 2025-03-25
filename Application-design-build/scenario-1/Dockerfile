FROM debian
WORKDIR /usr/local/app

#install git & python
RUN  apt update
RUN  apt install -y python3 python3-pip python3.11-venv git-all

#clone the repository 
RUN git clone https://github.com/pallets/flask
WORKDIR /usr/local/app/flask/examples/tutorial

RUN python3 -m venv venv

# install flask
RUN . venv/bin/activate && pip install -e .

# Initialize the database
RUN . venv/bin/activate && flask --app flaskr init-db

# # Initialize the database
# RUN . venv/bin/activate && flask init-db

# # Expose the port Flask runs on (default is 5000)
# EXPOSE 5000

# # Run the Flask development server
# CMD ["venv/bin/python", "-m", "flask", "run", "--debug", "--host=0.0.0.0"]