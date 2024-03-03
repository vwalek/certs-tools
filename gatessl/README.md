# gatessl

The `gatessl` command is a bash wrapper around `openssl` to list multiple certificates in one file. 

## Installation

Pull just the file into you `/.local/bin` directory.

~~~
# curl -o ~/.local/bin/gatessl https://https://raw.githubusercontent.com/vwalek/certs-tools/gatessl/gatessl

# chmod +x ~/.local/bin/gatessl
~~~

## Usage

~~~
Simple script to process multiple certificates in one file.
Wrapper around openssl command. 

Run:
# cat certs.pem | gatessl/gatessl [options] 

By default the command without options will show full human
readable format of the cert, like the openssl below.
# openssl x509 -noout -text

Options:
--help|-h               - Show the help/usage
--dates|-dates          - Show dates
--subject|-subject      - Show subject name
--issuer|-issuer        - Show the issuer
--san|-san              - Show the SAN section
--showcert|-showcert    - Show the certificate (inverse to -noout)

Examples:
# cat *.crt | gatessl/gatessl

# cat *.crt | gatessl/gatessl --dates --subject --issuer
~~~

# Notes

- The option `--san` will only work with `openssl` version 3.