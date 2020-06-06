first generate CSR and KEY:
openssl req -new -newkey rsa:4096 -nodes -keyout strapi-test.key -out strapi-test.csr

then generate PEM and self-sign with KEY:
openssl x509 -req -sha256 -days 365 -in strapi-test.csr -signkey strapi-test.key -out strapi-test.pem
