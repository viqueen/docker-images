FROM golang:1.24.4 AS go

RUN go install github.com/riverqueue/river/cmd/river@latest

ENV PATH="/usr/local/bin:${PATH}"

ENTRYPOINT ["river"]