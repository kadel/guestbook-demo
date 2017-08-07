
# 1st Stage - build binary

FROM golang:1.8
WORKDIR /go/src/github.com/kadel/kedge-demo/first/backend
COPY . .
RUN ls
RUN make build



# 2th Stage - create image

FROM centos:7

COPY --from=0 /go/src/github.com/kadel/kedge-demo/first/backend/server /opt/api/

EXPOSE 3000

ENV HOST 0.0.0.0
ENV DATA_FILE /opt/api/data/comments.json

RUN mkdir -p /opt/api/data/
RUN chmod a+w  /opt/api/data/

ENTRYPOINT ["/opt/api/server"]
