# Ansible: oracle-client

Setup Oracle client/library files

Available on Ansible Galaxy: [pgkehle.oracle-client](https://galaxy.ansible.com/pgkehle/oracle-client)

# Variables

```bash
client_pkg_dir: Local Install Folder.  Requires one of linux, macos, or win, with x32 and/or x64.

Example: 
    ~/downloads/oracle/client
    ~/downloads/oracle/client/linux
    ~/downloads/oracle/client/linux/x64
    ~/downloads/oracle/client/macos
    ~/downloads/oracle/client/macos/x64
    ~/downloads/oracle/client/win
    ~/downloads/oracle/client/win/x64
```  

# Examples

```yaml
- hosts: all

vars: 
  client_pkg_dir: ~/downloads/oracle/client
  do_install: true
  gather_facts: "{{ansible_host != 'localhost'}}"

roles:
  - pgkehle.oracle-client
```

## License

MIT

## Author Information

Paul Kehle  
@pgkehle ([twitter](https://twitter.com/pgkehle), [github](https://github.com/pgkehle), [linkedin](https://www.linkedin.com/in/pgkehle))

### References

Download [Instant Client from Oracle](http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html):
* [MacOS x64](http://www.oracle.com/technetwork/topics/intel-macsoft-096467.html)
* [Linux x64](http://www.oracle.com/technetwork/topics/linuxx86-64soft-092277.html)
    
#### Official OracleDB Node Package
* https://github.com/oracle/node-oracledb/blob/master/INSTALL.md#instosx
* https://github.com/oracle/node-oracledb/tree/master/examples
