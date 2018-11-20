# datadog-configs
Datadog collects various metrics on systems, services and apps.
Included here are configuration files for various Datadog-agent integrations.

## Installation directoy
`/etc/datadog-agent/conf.d/<integration>.d/<integration>.yaml`

e.g.
`/etc/datadog-agent/conf.d/tomcat.d/tomcat.yaml`

If adding a custom log collection e.g. `conf.d/tomcat_httpd.d/tomcat_http.yaml`: 
* Edit datadog.yaml: `sudo vi /etc/datadog-agent/datadog.yaml`
* Change the line: `# logs_enabled: false` to `logs_enabled: true`
* Save the file 


** Restart the Datadog agent **
After configuring the integration(s)/log collections, restart the Datadog agent


***RHEL 6***

`$ sudo restart datadog-agent`

***RHEL 7***

`$ sudo systemctl datadog-agent restart`

_OR_

`$ sudo service datadog-agent restart`