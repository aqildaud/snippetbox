### Generating a self-signed TLS certificate

To create a self-signed certificate using Go's standard library, follow these simplified steps:

1. **Locate the `generate_cert.go` file**:
   If you installed Go using the official instructions, you can find the file at:
     /usr/local/go/src/crypto/tls/generate_cert.go

3. **Run the tool**:
Use the following command to generate a certificate:
```bash
go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost
