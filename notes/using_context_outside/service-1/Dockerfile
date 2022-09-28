FROM docker/getting-started
RUN echo "=========== Start build image for service-1==========="
RUN env
COPY ./note.md .
RUN ls ./
ENTRYPOINT [ "echo", "parameter1" ]
# If ENTRYPOINT not existed, CMD has to be started with an executable
CMD [ "Default parameter if user not pass any parameter when run container" ]
