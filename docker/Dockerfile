FROM ipython/scipyserver
MAINTAINER Edward Kim <edward.junhyung.kim@gmail.com>
RUN apt-get update && \
    apt-get -y -q install libfftw3-dev libatlas-base-dev wget vim
RUN pip2 install --upgrade --no-deps git+git://github.com/Theano/Theano.git && \
    pip2 install --upgrade --no-deps git+git://github.com/Lasagne/Lasagne.git && \
    pip2 install --upgrade --no-deps git+git://github.com/dnouri/nolearn.git
RUN pip2 install --upgrade six pyyaml && \
    cd / && \
    git clone https://github.com/mclaughlin6464/pylearn2 && \
    cd pylearn2 && \
    python2 setup.py develop

RUN git clone https://github.com/Lasagne/Lasagne

ENV PYLEARN2_DATA_PATH /notebooks/ml-sims/data/

