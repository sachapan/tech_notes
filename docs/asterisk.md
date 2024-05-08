# Asterisk

## incrediblepbx specific

- Remove annoying firewall prompt

  Edit /root/.bashrc_profile PS1

## FreePBX specific

### Reset ARI username and password
```
fwconsole setting FPBX_ARI_USER 15-char-alphanum-string
fwconsole setting FPBX_ARI_PASSWORD 30-char-alphanum-string
fwconsole r
fwconsole restart
```
