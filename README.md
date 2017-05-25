# check_ansible-playbook
This script will check an ansible playbook and report the exit state in icinga or nagios.
ansible-playbook is used in order to perform this check and it you can execute a number of roles.

The scipts currently is used in a compliance environment, giving alerts in icinga2 when there is a deviation against a playbook.
All compliance intelligence is written in ansible, icinga2 is used to test all setting.
It can also be set in excution mode to change the settings in stead of checking.

The check is execute on the ansible server and will report the number ok changed failures skipped unreachable
If the ansible exit are not ok, this will be reported as an error.

If your playbook contains a lot of roles it might be usefull to tune the check frequency for this service. More info in the installation wiki.
