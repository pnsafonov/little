# Ansible Collection - lexx.little

Collection with general set of tasks.   

To use task from collection see example below.   
There is single role to import any task.

### Add collection as dependency
requirements.yml:
```yaml
collections:
  - name: lexx.little
    source: "https://github.com/pnsafonov/little.git"
    type: git
    version: 1.0.0
```

### Install or update pind service
Ansible playbook file:
```yaml
...
  tasks:
    - import_role:
        name: lexx.little.import
      vars:
        task_path: "tasks/service/pind/pind.yml"
...
```