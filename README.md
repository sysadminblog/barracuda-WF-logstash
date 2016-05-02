Barracuda Web Filter logstash filters.

These were built for a Web Filter 410 vX, they should work for other models too.

For more details see my blog post about this here: https://sysadminblog.net/2016/05/barracuda-web-filter-logstash/

## Usage

Add the filter files to your logstash configuration directory, eg. `/etc/logstash/conf.d`.

Log into your Barracuda Appliance and go to the Advanced tab and click Syslog. Set up both the Web Interface and Web Traffic syslogs to point to your logstash server.

You must edit the `05-syslog-parse_barracuda.conf` file and set the correct IP address of your web filter.

## Files

### 05-syslog-parse_barracuda.conf

This file will do an initial parse of the syslog entry.

### 20-barracuda.conf

This file will grok the syslog entry and pull out all the useful information.
