# Postfix

## gmail as relayhost






Enforce tls

`echo "smtp.gmail.com encrypt" >> /etc/postfix/tls_policy`

`postmap /etc/postfix/tls_policy`

in main.cf:

`smtp_use_tls = yes
smtp_sasl_auth_enable = yes
smtp_sasl_security_options = noanonymous
smtp_sasl_tls_security_options = noanonymous
smtp_sasl_password_maps = hash:/etc/postfix/sasl/sasl_passwd
smtp_tls_CAfile = /etc/ssl/certs/ca-certificates.crt`


Allow non-tls for some relays

`smtp_tls_security_level = may`

## Direct some domains to alternate relayhost

In my case, I route some messages to a [mailrise](https://github.com/YoRyan/mailrise) instance on my LAN.

`echo "mailrise.xyz smtp:mailrise_host" >> /etc/postfix/transport`

`postmap /etc/postfix/transport`

Add to /etc/postfix/main.cf:

`transport_maps = hash:/etc/postfix/transport`



## Managing the queue

mailq equivalent

`postqueue -p`

flush queue

`postqueue -f`

Delete a message from the queue

`postsuper -d <MESSAGEID>`

where MESSAGEID is obtained from `postqueue -p`

  
