# openssl-commands


# openssl-convert-pfx-to-key
```
openssl pkcs12 -in abc.pfx -nocerts -out abc.key
```

# openssl-convert-pfx-to-crt

```
openssl pkcs12 -in abc.pfx -clcerts -nokeys -out abc.cer
```

# openssl-create-pfx-without-password

enter blank as password for new pfx

```
openssl pkcs12 -export -keypbe NONE -certpbe NONE -in abc.cer -inkey abc.key -out abc_wop.pfx

```
