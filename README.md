# awx-demo
Just a demo of using https://galaxy.ansible.com/redhat_cop/controller_configuration

## Usage
```
ansible-navigator run -i inventory --eei <EE> --mode stdout --pae false configure_controller.yml
```

## Notes
- The `mode` and `pae` options are due to the use of `vars_prompt` in the playbook. If your use case eliminates this, then those options can be omitted.
- There are other ways you can run this other than with `ansible-navigator`, that's just what I'm using in this example.
- There is a `<EE>` placeholder in the `ansible-navigator` command above. An appropriate Execution Environment containing the `ansible.controller` and `redhat_cop.controller_configuration` collections is required. The `ee` directory in this repo contains what you'd need to build one using [ansible-builder](https://www.ansible.com/blog/introduction-to-ansible-builder).
