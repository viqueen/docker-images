FROM golang:1.23.5 AS go

RUN go install github.com/riverqueue/river/cmd/river@latest

ENV PATH="/usr/local/bin:${PATH}"

ENTRYPOINT ["river"]