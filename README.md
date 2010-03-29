SCRIPT
================

* generate-cidr-files
  * generate following files from original data.
    * yaml
      * YAML in one file
    * pair
      * plain text, CIDR and block name in one line (for Nginx geo module).

* update-mobilejp-cidr
  * based: http://cpansearch.perl.org/src/TOKUHIROM/Net-CIDR-MobileJP-0.17/net-cidr-mobilejp-scraper.pl

USAGE
================

    update-mobilejp-cidr -o /etc/ip.d/plain/ && generate-cidr-files -i /etc/ip.d/plain/ -d /etc/ip.d/

