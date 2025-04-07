# RSA_gen

# RSA Key Generator

A Python script to generate secure RSA key pairs (2048-bit) using the `cryptography` library. This tool creates a private key and its corresponding public key, saving them in PEM format to files for use in cryptographic applications.

## Features
- Generates 2048-bit RSA key pairs with a public exponent of 65537
- Outputs keys in PEM format:
  - Private key: `private_key.pem` (unencrypted)
  - Public key: `public_key.pem`
- Includes basic error handling for key generation and file operations
- Modular design for easy extension (e.g., adding encryption/decryption)

## Prerequisites
- Python 3.6+
- `cryptography` library

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/rsa-key-generator.git
   cd rsa-key-generator
   ```
2. Install the required library:
   ```bash
   pip install cryptography
   ```

## Usage
Run the script to generate and save RSA keys:
```bash
python rsa_key_generator.py
```

### Output
- Two files will be created in the current directory:
  - `private_key.pem`: The private key
  - `public_key.pem`: The public key
- Console output:
  ```
  RSA keys (2048-bit) generated and saved to 'private_key.pem' and 'public_key.pem'.
  ```

### Example Files
- **Private Key** (`private_key.pem`):
  ```
  -----BEGIN RSA PRIVATE KEY-----
  [Base64-encoded key data]
  -----END RSA PRIVATE KEY-----
  ```
- **Public Key** (`public_key.pem`):
  ```
  -----BEGIN PUBLIC KEY-----
  [Base64-encoded key data]
  -----END PUBLIC KEY-----
  ```

## Notes
- **Security**: The private key is saved unencrypted. For production use, consider adding passphrase encryption (see [Future Improvements](#future-improvements)).
- **Key Size**: Default is 2048 bits, suitable for most applications. Larger sizes (e.g., 4096) can be implemented by modifying `key_size`.
- **Compatibility**: PEM files are compatible with tools like OpenSSL.

## Future Improvements
- Add encryption/decryption functionality for messages using the generated keys.
- Support passphrase encryption for the private key.
- Allow custom filenames and key sizes via command-line arguments.

## Contributing
Feel free to fork this repository, submit issues, or send pull requests with enhancements!

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Built with the `cryptography` library: [https://cryptography.io/](https://cryptography.io/)
```
