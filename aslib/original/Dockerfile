FROM rocker/r-ver:4.0.0-ubuntu18.04

# system libraries of general use
RUN apt-get update && apt-get install -y \
    sudo \
		pandoc \
		pandoc-citeproc \
		libxml2-dev \
		libcurl4-gnutls-dev \
		libcairo2-dev \
		libxt-dev \
		libssl-dev \
		libssh2-1-dev \		
		subversion \
		git \
		default-jdk \
		default-jre \
	&& R CMD javareconf		


# install R packages
RUN R -e "install.packages('aslib')"

# get aslib repo
RUN mkdir home/aslib
RUN mkdir home/aslib-spec
RUN git clone https://github.com/coseal/aslib-r.git home/aslib
RUN git clone https://github.com/coseal/aslib-spec.git home/aslib-spec
