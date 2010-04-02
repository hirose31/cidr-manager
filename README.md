SCRIPT
================

* generate-cidr-files
  * generate following files from original data.
    * yaml
      * YAML in one file
    * pair
      * plain text, CIDR and block name in one line (for Nginx's geo module).

* update-mobilejp-cidr
  * based: http://cpansearch.perl.org/src/TOKUHIROM/Net-CIDR-MobileJP-0.17/net-cidr-mobilejp-scraper.pl

USAGE
================

    update-mobilejp-cidr -o /etc/ip.d/plain/ -f notifier@example.com -e tommy@example.com -e matsu@example.org && generate-cidr-files -i /etc/ip.d/plain/ -o /etc/ip.d/

      If find new CIDR info for any mobile carrier, update-mobilejp-cidr do:
        * write into files under /etc/ip.d/plain/
        * notify by email
        * exit 0
      and generate-cidr-files do:
        * read from  /etc/ip.d/plain/*
        * write into /etc/ip.d/yaml/cidr
        * write into /etc/ip.d/pair/cidr

