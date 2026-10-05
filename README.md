# GOAD-Light (Game of Active Directory)

GOAD-Light by [Orange Cyberdefense](https://github.com/Orange-Cyberdefense/GOAD): one forest, two
domains, three Windows Server 2019 machines. This repository runs it with
[Isoloom](https://www.isoloom.com): [`isoloom.yml`](isoloom.yml) describes the machines, and GOAD's
own Ansible playbooks build the lab from a controller.

| Machine | Name | Domain |
| --- | --- | --- |
| dc01 | KINGSLANDING | sevenkingdoms.local |
| dc02 | WINTERFELL | north.sevenkingdoms.local |
| srv02 | CASTELBLACK | north.sevenkingdoms.local (IIS, MSSQL) |

## Run it

```bash
isoloom generate
cd .isoloom/vagrant && vagrant up
```

Built end to end this way on VirtualBox, with no failed task. About 13 GB of memory (11.7 GB for
the three machines, 1 GB for the controller). Lab guide: the
[GOAD documentation](https://orange-cyberdefense.github.io/GOAD/).

## Licence

GPL-3.0, as GOAD ([LICENSE](LICENSE)). This lab is deliberately vulnerable: keep it isolated.
