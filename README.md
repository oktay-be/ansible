# amsible repository


sudo ansible-playbook \
--vault-id infra@/Users/user/certificate/ansible_infra_password \
-i inventory/dev/hosts.ini \
-e execution_mode=install \
-e target_host=dev-kubernetes-master \
-e ansible_user=oktay \
playbooks/cron/k8s/scale.yml \
-vv

sudo ansible-playbook \
--vault-id infra@/Users/user/certificate/ansible_infra_password \
-i inventory/dev/hosts.ini \
-e execution_mode=uninstall \
-e target_host=dev-kubernetes-master \
-e ansible_user=oktay \
playbooks/cron/k8s/scale.yml \
-vv
