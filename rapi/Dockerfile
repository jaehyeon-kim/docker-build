FROM rocker/tidyverse:3.5.1

## rserve
RUN apt-get update \
  && apt-get install -y libssl-dev wget curl procps \
  && wget https://www.rforge.net/src/contrib/Rserve_1.8-6.tar.gz \
  && /usr/local/bin/R CMD INSTALL Rserve_1.8-6.tar.gz

RUN R -e 'install.packages(c("data.table", "jsonlite", "logging", "lubridate"))'

RUN useradd -ms /bin/bash api
