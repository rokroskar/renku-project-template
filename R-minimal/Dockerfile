FROM renku/singleuser-r:0.4.3-renku0.8.2

# Uncomment and adapt if code is to be included in the image
# COPY src /code/src

# Uncomment and adapt if your R or python packages require extra linux (ubuntu) software
# e.g. the following installs apt-utils and vim; each pkg on its own line, all lines
# except for the last end with backslash '\' to continue the RUN line
# 
# USER root
# RUN apt-get update && \
#    apt-get install -y --no-install-recommends \
#    apt-utils \
#    vim
# USER ${NB_USER}

# install the R dependencies
COPY install.R /tmp/
RUN R -f /tmp/install.R

# install the python dependencies
COPY requirements.txt /tmp/
RUN pip3 install -r /tmp/requirements.txt
