FROM ubuntu

RUN apt update
RUN echo "y" | apt install proftpd-basic proftpd-core

RUN useradd -m dev


RUN echo "dev" >> mdp && echo "dev" >> mdp
RUN passwd dev < mdp

COPY permissions.sh /

ENTRYPOINT ["/permissions.sh"]

CMD ["proftpd", "--nodaemon"]
