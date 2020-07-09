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





                  OR
```
openssl pkcs12 -in MyCertificate.pfx -clcerts -nokeys -out MyCertificate.crt
openssl pkcs12 -in MyCertificate.pfx -nocerts -out MyCertificate-encrypted.key
openssl rsa -in MyCertificate-encrypted.key -out MyCertificate_unenc.key
openssl pkcs12 -export -out MyCertificate_np.pfx -inkey MyCertificate_unenc.key -in MyCertificate.crt -passout pass:

```
