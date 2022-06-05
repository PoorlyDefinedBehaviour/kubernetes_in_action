FROM ubuntu:latest
RUN apt-get update; apt-get -y install fortune
ADD fortuneloop.sh /bin/fortuneloop.sh
ENTRYPOINT [ "/bin/fortuneloop.sh" ]
# the default argument for the executable
CMD ["10"] 