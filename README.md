# Ansible Role - oracle-client

Setup Oracle client/library files

Available on Ansible Galaxy: [isaackehle.oracle-client](https://galaxy.ansible.com/isaackehle/oracle-client)

## Variables

```bash
oracle_clients: Local Install Folder.  Requires one of linux, macos, or win, with x32 and/or x64.

Example Layout:
  ~/downloads/oracle/client/linux
  ~/downloads/oracle/client/linux/x64
  ~/downloads/oracle/client/macos
  ~/downloads/oracle/client/macos/x64
  ~/downloads/oracle/client/win
  ~/downloads/oracle/client/win/x64
```

## Examples

```yaml
- hosts: all
  gather_facts: inventory_hostname != 'localhost'
  vars:
    oracle_clients: ~/Downloads/oracle/client
  roles:
    - { role: isaackehle.oracle-client }
```

## Linting

```bash
yamllint -c yamllint.yaml .
ansible-lint .
```

## License

MIT

## Author Information

Isaac Kehle
@isaackehle ([twitter](https://twitter.com/isaackehle), [github](https://github.com/isaackehle), [linkedin](https://www.linkedin.com/in/isaackehle))

### References

Download [Instant Client from Oracle](http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html):

- [MacOS x64](http://www.oracle.com/technetwork/topics/intel-macsoft-096467.html)
- [Linux x64](http://www.oracle.com/technetwork/topics/linuxx86-64soft-092277.html)

#### Official OracleDB Node Package

- [oracle install osx](https://github.com/oracle/node-oracledb/blob/master/INSTALL.md#instosx)
- [oracle examples](https://github.com/oracle/node-oracledb/tree/master/examples)
