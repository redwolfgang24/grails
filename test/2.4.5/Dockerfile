FROM java:7
MAINTAINER Larry Borrero <redwolfgang20@gmail.com>

ARG GRAILS_VERSION=2.4.5

# Install Grails
WORKDIR /usr/lib/jvm

ADD https://github.com/grails/grails-core/releases/download/v$GRAILS_VERSION/grails-$GRAILS_VERSION.zip /usr/lib/jvm/grails-$GRAILS_VERSION.zip
RUN unzip grails-$GRAILS_VERSION.zip
RUN rm -rf grails-$GRAILS_VERSION.zip
RUN ln -s grails-$GRAILS_VERSION grails

# Setup Grails path.
ENV GRAILS_HOME /usr/lib/jvm/grails
ENV PATH $GRAILS_HOME/bin:$PATH

WORKDIR /

# Set Default Behavior
ENTRYPOINT ["grails"]
