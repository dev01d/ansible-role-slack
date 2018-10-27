# Ansible role Slack

![Slack screen shot](assets/screen-shot.png?raw=true 'Title')

This role allows the addition of modular slack notifications to ansible playbooks.

```yaml
- hosts: '{{ host }}'
  become: yes
  vars:
    host: # Host group
  # Set facts for role digest
  pre_tasks:
    - name: Setting repo facts
      set_fact:
        slack_token: XXXX/YYYY/ZZZZ
        message: Updates completed on {{ inventory_hostname }}
  roles:
    # - Invoke role for slack to report on
    - slack
```
