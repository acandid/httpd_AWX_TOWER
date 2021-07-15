Apache
=======

This playbook can be used on AWX or Tower
Install and configuring the Apache SSL on RHEL/CentOS, Debian 9,10 and Ubuntu 20.04

- Install the necessary packages;
- Configure apache, vhost and ssl.

Requirements
------------

- The SELinux and firewall settings are not considered to be a concern of this role.

Role Variables
--------------

Necessary changes to defaults/main.yml

| Variables                                    | Defaults                      | Comments
| :---                                         | :---                          | :---                                                    
| `httpd_AWX_TOWER_docroot`                    | '/var/www/html'               | Path to the document root (directory containing html files)
|                                              |                               |
| `httpd_AWX_TOWER_domain`                     |                               | Inform your domain
|                                              |                               |

Variables that can be changed if you want.
For Red Hat family:

| Variables                                    | Defaults
|:---                                          |:---
| `httpd_AWX_TOWER_errorlog`                   | /var/log/httpd/
|                                              |
| `httpd_AWX_TOWER_customlog`                  | /var/log/httpd/
|                                              |
| `httpd_AWX_TOWER_cert_path`                  | /etc/pki/tls/certs/
|                                              |
| `httpd_AWX_TOWER_vhost_path`                 | /etc/httpd/conf.d/
|                                              |

Variables that can be changed if you want.
For Debian family:

| Variables                                    | Defaults
|:---                                          |:---
| `httpd_AWX_TOWER_errorlog`                   | /var/log/apache2/
|                                              |
| `httpd_AWX_TOWER_customlog`                  | /var/log/apache2/
|                                              |
| `httpd_AWX_TOWER_cert_path`                  | /etc/ssl/certs/
|                                              |
| `httpd_AWX_TOWER_vhost_path`                 | /etc/apache2/sites-available/
|                                              |

Dependencies
------------

No dependencies.

Installing Certificates
-----------------------

It is necessary to exchange the certificates below for your certificates

```
├── files
│   ├── almircandido.com_ca.crt
│   ├── almircandido.com.crt
│   └── almircandido.com.key

```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido/
