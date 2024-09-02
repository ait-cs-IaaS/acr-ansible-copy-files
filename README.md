# Ansible-Role: acr-ansible-copy-files

AIT-CyberRange: Copies files and directories to remote host. 


## Requirements

- Debian or Ubuntu 

## Role Variables

```yaml
files_basedir: /path/on/localhost/
files_subfolders:
  - subdir
files_destination: /path/on/remote/machine
files_owner: username
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - acr-ansible-copy-files
      vars:
        files_basedir: "{{ local_ansible_dir }}/data/desktop_files/"
        files_subfolders: '{{ desktop_files }}'
        files_owner: "{{ client_user.username }}"
        files_destination: /home/{{ client_user.username }}/Desktop/
```

## License

GPL-3.0

## Author

- Lenhard Reuter