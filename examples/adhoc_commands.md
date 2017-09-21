# Workshop: Ad-Hoc Commands

### Answer

```
ansible all -i albertwong-instances.txt -m yum -a "name=https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm state=present enablerepo=epel" -b --limit web
ansible web -i albertwong-instances.txt -m command -a "yum repolist all" -b
```
