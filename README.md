# Ansible Java Role

Manages installations of Java JREs and JDKs, supporting both OpenJDK and Oracle JRE and JDK 6, 7, and 8.

## Requirements and Dependencies

None.

## Role Variables

```yaml
java_packages:
  - openjdk-7-jre
  - openjdk-8-jre
```

Valid packages include:

* openjdk-6-jre
* openjdk-6-jre-headless
* openjdk-6-jdk
* openjdk-7-jre
* openjdk-7-jre-headless
* openjdk-7-jdk
* openjdk-8-jre
* openjdk-8-jre-headless
* openjdk-8-jdk
* oracle-java6-installer
* oracle-java7-installer
* oracle-java8-installer

For 32-bit versions, append `:i386` to the package names.  If you're installing Oracle JDK and want it to be the default, add `oracle-java6-set-default`, `oracle-java7-set-default` or `oracle-java6-set-default` to the `java_packages` list.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - java
```
