
# ansible_dnsexit

An example of maintaining a simple DNSEXIT Dynamic DNS Domain using Ansible.  

## The use case

I have a DNSEXIT domain I use for my home server.  Let's call it mydomain.linkpc.net.  I use the domain A record for my web server, and a TXT record to perform ownership verification for mydomain.linkpc.net when using certbot to request a new SSL Certificate from letsencrypt.  I use the following command:

    # certbot certonly --manual --manual-auth-hook /etc/letsencrypt/acme-dns-auth.py --preferred-challenges dns --debug-challenges -d mydomain.linkpc.net -v
