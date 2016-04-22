# Ansible Role - blast

This playbook installs [NCBI BLAST](http://blast.ncbi.nlm.nih.gov/Blast.cgi).

## Platforms

CentOS 6.7 is the only platform that is supported and tested so far.
CentOS 7 will be added soon.

## Role Variables

- Check out [defaults/main.yml](defaults/main.yml)

## Dependencies

None.

## Installation

Regular installation:

```
ansible-galaxy install RDI2.blast
```

Installation to a specific directory(e.g. roles/):

```
ansible-galaxy install -p roles/ RDI2.blast
```

## Example Playbook

    - hosts: servers
      roles:
         - { role: RDI2.blast }

## License

MIT License.

## Author

- Koji Tanaka, RDI2
