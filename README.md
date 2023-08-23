# MailHog

MailHog is an email testing tool that makes it super easy to install and configure a local email server. MailHog sets up a fake SMTP server. You can configure your preferred web applications to use MailHog’s SMTP server to send and receive emails.
## Default login and password

```bash
username: admin
password: admin_pass

```


## Change login and password


```bash
printf "admin:" > /home/mailhog.auth
printf "$(sudo docker exec  mailhog-smtp2-mailhog-1 /bin/sh -c "MailHog bcrypt admin_pass")" >> /home/mailhog.auth
```

## Usage

To ensure the availability of the service's URL address, you can utilize this project [jwilder/docker-gen](https://hub.docker.com/r/jwilder/docker-gen).

To achieve this, please uncomment the following parameters and enter the desired values:

```python
 - VIRTUAL_HOST=smtp.domian.com
 - LETSENCRYPT_HOST=smtp.domain.com
 - VIRTUAL_PORT=8025      
```
