# check_ansible-playbook
This script will check an ansible playbook and report the exit state of the ansiple-playbook run.
The ansible-playbook is used in order to perform this check and it will execute a number of roles.

The scipts currently is used in a compliance environment, giving alerts in icinga2 when there is a deviation against a playbook.
All compliance intelligence is written in ansible, icinga2 is used to test all setting.  

The check is execute on the ansible server and will report the number ok changed failures skipped unreachable
If the ansible exit are not ok, this will be reported as an error.
