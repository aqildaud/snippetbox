### Generating a self-signed TLS certificate

To create a self-signed certificate using **Go's standard library**, follow these simplified steps:
1. First create a new `tls` directory in the `root` of your project repository to hold the certificate and change into it:
   ```bash
   /your-project-directory
   mkdir tls
   cd tls
   
1. **Locate the** `generate_cert.go` **file**:
   If you installed Go using the official instructions, you can find the file at:
     `/usr/local/go/src/crypto/tls/generate_cert.go`

3. **Run the tool**:
   Use the following command to generate a certificate:
   ```bash
   go run /usr/local/go/src/crypto/tls/generate_cert.go --rsa-bits=2048 --host=localhost

4. Behind the scenes the `generate_cert.go` tool works in two stages:
   1. First, it creates a secure 2048-bit RSA key pair.
   2. The private key is saved in `key.pem`, and a self-signed TLS certificate for `localhost` is generated with the public key, saved in `cert.pem`. Both files are PEM encoded, which is standard for TLS.
   3. Your repository should now look something like this:  
      ```
      tls/  
      ├── cert.pem  
      └── key.pem  
