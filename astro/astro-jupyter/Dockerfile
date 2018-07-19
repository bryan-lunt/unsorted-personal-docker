FROM jupyter/scipy-notebook

LABEL maintainer="Bryan J. Lunt <bjlunt2@illinois.edu>"

USER root

#RUN apt-get install -y xephem

USER $NB_UID


RUN conda config --add channels conda-forge \
	&& conda config --add channels http://ssb.stsci.edu/astroconda \
	&& conda install --quiet --yes gsl nlopt pygmo pygmo_plugins_nonfree iminuit \
		yt \
		cspice spiceypy pyephem astroplan pyorbital \
		astropy	astropy-healpix \
		pykep \
		poliastro \
		astroquery astroml \
		astro-gala \
	&& pip install krpc


