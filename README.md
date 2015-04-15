Playbook
========

Sets up a nginx proxy specifically to forward POSTs to /github-webhook
to the internal Jenkins host.

Variables
---------

 - jenkins_host: (default="cgjenkins.svc.spsdev.in") the host to proxy requests to
 - proxy_server_name: (default="cg-jenkins-proxy.spsc.io") the server_name/hostname of the proxy
 - jenkins_timeout: (default=5) the number of seconds to wait when testing the Jenkins host post is open
 - proxy_timeout: (default=5) the number of seconds to wait when testing the proxy port is open
 - listen_port: (default=80) this should be 443 but we'll need to add SSL cert stuff then. DO THIS
 - poll_interval: (default=2) seconds between iterations when polling for output from both the proxy and the jenkins host
 - nginx_servers: Stouts.nginx variable to configure the nginx server blocks. Defaults to a proxy


Dependencies
------------

Stouts.nginx

