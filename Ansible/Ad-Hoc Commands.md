# Ad-Hoc Commands
Fast one-line Ansible commands.
Used when:

* You don’t want a full playbook
* Quick checks
* Emergency fixes
* Testing connectivity

Ping all servers
----
ansible all -m ping

Install nginx
----
ansible web -m apt -a "name=nginx state=present" -b

Check disk usage
----
ansible all -a "df -h"

Restart service
----
ansible web -m service -a "name=nginx state=restarted" -b
