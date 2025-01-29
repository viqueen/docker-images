FROM bufbuild/buf:1.49.0 AS buf


FROM golang:1.23.1 AS go

RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.36.2
RUN go install connectrpc.com/connect/cmd/protoc-gen-connect-go@v1.18.1

COPY --from=buf /usr/local/bin/buf /usr/local/bin/buf

ENV PATH="/usr/local/bin:${PATH}"

ENTRYPOINT ["buf"]