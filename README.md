# zabbix-docker
Web server will be up on http://ipaddress:8282 but can be changed

You need a .env in your compose folder with value mappings.
.env file alos need to run the docker file.


Zabbix Agent:
Version 1 (Basic Configuration)
Zabbix agent installed without additional privileges.
Limited to network-level checks and basic system metrics; cannot monitor detailed Docker metrics or other containers’ internals.
Offers the highest level of security due to lack of elevated access.
Version 2 (Docker Socket Access)
Zabbix agent within a container has access to the Docker socket.
Enables monitoring of Docker daemon and containers, providing detailed insights into container statuses, resource usage, and more.
Increased security risk due to elevated access. Needs careful security measures to mitigate potential vulnerabilities.
Version 3 (Host Filesystem and /var/run Access)
Zabbix agent within a container has access to the host’s entire filesystem and /var/run.
Allows for comprehensive monitoring of the host system and Docker environment, including detailed system and Docker metrics.
High security risk because of privileged access. Requires strict security control and monitoring to safeguard the system.
