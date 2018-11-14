FROM  cyberdojofoundation/gcc
LABEL maintainer=byran@adgico.co.uk

# Ruby is needed for the script that builds the main function

RUN apt-get update && apt-get install -y \
  ruby

# Install utilities to download the unit test framework

RUN apt-get update && apt-get install -y \
  wget \
  unzip

# Download and extract Unity, there is no version labelling on the ThrowTheSwitch/Unity GitHub
# repository so download from my fork that has version tags espically for cyberdojo

WORKDIR /

RUN wget https://github.com/byran/Unity/archive/v2.4.3.zip
RUN unzip v2.4.3.zip
RUN mv Unity-2.4.3 unity

COPY red_amber_green.rb /usr/local/bin
