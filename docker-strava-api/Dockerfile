FROM dockerfile/python

RUN wget -O /tmp/requirements.txt https://raw.githubusercontent.com/ssteveli/stravasocial/master/app/api/requirements.txt
RUN pip install -r /tmp/requirements.txt
RUN pip install Flask-JWT
RUN pip install beaker

RUN cd /tmp; git clone https://github.com/ssteveli/stravalib.git
RUN cd /tmp/stravalib; python setup.py install

ENV PYTHONPATH /data/stravasocial/app
CMD python /data/stravasocial/app/api/api.py
