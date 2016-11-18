# How to use it
0. You must have ansible installed locally.
1. Clone the repository locally.
2. Change the ip's in the hosts directory files.
3. Change the group_vars settings.
4. Check the vars folder settings in order to make sure that you are ok with the defaulted settings.
5. Run the playbook on the desired host:
    - ansible-playbook -i ansible/provisioning/hosts/staging playbook.yml
    - ansible-playbook -i ansible/provisioning/hosts/production playbook.yml

# What to expect
This playbook will install all the needed elements for a Laravel 5 application. Is been currently tested on a Laravel 5.1 using queues and workers.

- NGINX
- PHP
- MYSQL
- REDIS
- Laravel queues
- Laravel worker
- Cron job to run schedule:run (every minute)
- PYTHON

# Notes
The nginx defaults to the 80 port (a.k.a http), I intend to add a block for https in the future.
As a side note I will say that this works really well in conjunction with the deploy script: [envoy-deployscript](https://github.com/nickfan/envoy-deployscript)

# Credits
This playbook is based on multiple roles. All the credit for those go to their creators.

# Disclaimer
THE PROGRAM IS DISTRIBUTED IN THE HOPE THAT IT WILL BE USEFUL, BUT WITHOUT ANY WARRANTY. IT IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

IN NO EVENT THE AUTHOR WILL BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF THE AUTHOR HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.