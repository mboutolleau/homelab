# Cerbot Docker Compose Configuration

## Usage

To get a SSL certificate for the domain `<domain>`, using the Let's Encrypt CA, without registering an email an by aggreing their TOS :

- Let's Encrypt Staging Area (testing/debug)
        
      sudo docker-compose run certbot certonly --webroot --register-unsafely-without-email --agree-tos --webroot-path=/var/www --staging -d <domain>

- Production (let's rock !)

      sudo docker-compose run certbot certonly --webroot --register-unsafely-without-email --agree-tos --webroot-path=/var/www -d <domain>