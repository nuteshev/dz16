Результат команды list jobs:

```
*list jobs
Automatically selected Catalog: MyCatalog
Using Catalog "MyCatalog"
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
| JobId | Name          | StartTime           | Type | Level | JobFiles | JobBytes   | JobStatus |
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
|     1 | BackupClient2 | 2020-12-31 01:40:02 | B    | F     |    2,412 | 10,525,063 | T         |
|     4 | BackupClient2 | 2020-12-31 02:10:00 | B    | I     |        0 |          0 | f         |
|     2 | BackupClient2 | 2020-12-31 02:17:36 | B    | F     |    2,412 | 10,525,063 | T         |
|     3 | BackupClient2 | 2020-12-31 02:17:41 | B    | F     |    2,412 | 10,525,063 | T         |
|     5 | BackupClient2 | 2020-12-31 02:20:02 | B    | I     |        0 |          0 | T         |
|     6 | BackupClient2 | 2020-12-31 02:30:03 | B    | D     |        0 |          0 | T         |
|     7 | BackupClient2 | 2020-12-31 02:40:02 | B    | I     |        0 |          0 | T         |
|     8 | BackupClient2 | 2020-12-31 02:50:02 | B    | I     |        0 |          0 | T         |
|     9 | BackupClient2 | 2020-12-31 03:00:02 | B    | D     |        9 |     13,856 | T         |
|    10 | BackupClient2 | 2020-12-31 03:10:02 | B    | I     |        0 |          0 | T         |
|    11 | BackupClient2 | 2020-12-31 03:20:02 | B    | I     |        0 |          0 | T         |
|    12 | BackupClient2 | 2020-12-31 03:30:02 | B    | D     |        9 |     13,856 | T         |
|    13 | BackupClient2 | 2020-12-31 03:40:02 | B    | I     |        0 |          0 | T         |
|    14 | BackupClient2 | 2020-12-31 03:50:02 | B    | I     |        0 |          0 | T         |
|    15 | BackupClient2 | 2020-12-31 04:00:02 | B    | D     |        9 |     13,856 | T         |
|    16 | BackupClient2 | 2020-12-31 04:10:02 | B    | I     |        0 |          0 | T         |
|    17 | BackupClient2 | 2020-12-31 04:20:02 | B    | I     |        0 |          0 | T         |
|    18 | BackupClient2 | 2020-12-31 04:30:02 | B    | D     |        9 |     13,856 | T         |
|    19 | BackupClient2 | 2020-12-31 04:40:02 | B    | I     |        0 |          0 | T         |
|    20 | BackupClient2 | 2020-12-31 04:50:02 | B    | I     |        0 |          0 | T         |
|    21 | BackupClient2 | 2020-12-31 05:00:02 | B    | D     |        9 |     13,856 | T         |
+-------+---------------+---------------------+------+-------+----------+------------+-----------+
You have messages.
```

Пример вывода list files jobid (для дифференциальных бэкапов). 

```
*list files jobid=21
+----------+
| Filename |
+----------+
| /etc/ssh/ |
| /etc/ssh/sshd_config |
| /etc/bacula/ |
| /etc/bacula/bacula-fd.conf |
| /etc/bacula/fd-example.cert |
| /etc/bacula/fd-example.key |
| /etc/bacula/fd-example.pem |
| /etc/bacula/master.cert |
| /etc/bacula/master.key |
+----------+
+-------+---------------+---------------------+------+-------+----------+----------+-----------+
| JobId | Name          | StartTime           | Type | Level | JobFiles | JobBytes | JobStatus |
+-------+---------------+---------------------+------+-------+----------+----------+-----------+
|    21 | BackupClient2 | 2020-12-31 05:00:02 | B    | D     |        9 |   13,856 | T         |
+-------+---------------+---------------------+------+-------+----------+----------+-----------+
```

Эти файлы я менял, т.к. добавил шифрование бэкапов не с самого начала. 

Конфиги клиента и сервера лежат в папках client и server. 