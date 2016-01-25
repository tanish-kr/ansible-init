# ansible init script

## Description
ansible layouts template generation script

## Environment

- serverspec (>= 2.17)
- ansible (>= 2.0.0)
- python (~> 2.7)

## Exec

```console
$ ansible-init -p test -b centos/7 -i 192.168.111.1 -m 2048 -c 1
```

## Usage

```
usage: ansible-init [-h] -p PLAYBOOK_NAME [-b BOX_NAME] [-i IP_ADDR]
                    [-m MEMORY] [-c CPU]
```
                    

## Options

```
optional arguments:
  -h, --help            show this help message and exit
  -p PLAYBOOK_NAME, --playbook_name PLAYBOOK_NAME
                        playbook name
  -b BOX_NAME, --box_name BOX_NAME
                        vagrant box name
  -i IP_ADDR, --ip_addr IP_ADDR
                        private ip address
  -m MEMORY, --memory MEMORY
                        box memory
  -c CPU, --cpu CPU     box cpu
```

## Generated files

```
.
├── Rakefile
├── Vagrantfile
├── filter_plugins
├── group_vars
├── host_vars
├── library
├── roles
│   └── test
│       ├── defaults
│       │   └── main.yml
│       ├── files
│       ├── handlers
│       │   └── main.yml
│       ├── meta
│       │   └── main.yml
│       ├── tasks
│       │   └── main.yml
│       ├── templates
│       │   └── template.conf.j2
│       └── vars
│           └── main.yml
├── spec
│   ├── default
│   │   └── sample_spec.rb
│   └── spec_helper.rb
└── test-playbook.yml

```

