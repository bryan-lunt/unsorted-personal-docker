FROM astro-jupyter

LABEL maintainer="Bryan J. Lunt <bjlunt2@illinois.edu>"

USER root

#RUN apt-get install -y xephem

USER $NB_UID


RUN conda config --add channels conda-forge \
	&& conda config --add channels http://ssb.stsci.edu/astroconda \
	&& conda install --quiet --yes iraf-all pyraf-all stsci


