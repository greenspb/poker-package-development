FROM rocker/r-base

# install system dependencies for RStudio
RUN apt-get update && apt-get install -y --no-install-recommends \
  libcurl4-openssl-dev \
  libssl-dev \
  libxt-dev \
  libpng-dev \
  libjpeg-dev \
  libtiff-dev \
  fonts-liberation

# install RStudio (using the official RStudio package manager)
RUN apt-get install -y r-base-dev
RUN wget https://download1.rstudio.org/electron/jammy/amd64/rstudio-2025.05.1-513-amd64.deb
RUN dpkg -i rstudio-2025.05.1-513-amd64.deb
RUN apt-get install -f -y # Fix any dependency issues

# Set working directory (optional)
#WORKDIR /app

# Expose the RStudio port
EXPOSE 8787
