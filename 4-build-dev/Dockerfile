FROM python
RUN useradd www && \
    mkdir /app && \
    mkdir /log && \
    chown www /log

USER www
VOLUME /log
WORKDIR /app
EXPOSE 8000

ENTRYPOINT ["/usr/local/bin/python"]
CMD ["run.py"]

# docker container run -it -v C:\Users\Marco\Documents\Git\docker-lab\4-build-dev:/app -p 80:8000 --name python-server build-dev

# acessando o conteúdo mapeado no volume do container anterior a partir de outro container:
# docker run -it --volumes-from=build-dev debian cat /log/http-server.log