FROM renku/singleuser:0.2.0

# Uncomment and adapt if code is to be included in the image
# COPY src /code/src

# install the python dependencies
COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt
