1. Измените параметры в файле по пути `database/config.py` следующим образом:

```python
    'dbname': 'ваше_название',
    'user': 'ваш_пользователь (по умолчанию postgres)',
    'password': 'ваш_пароль',
    'host': 'localhost',
    'port': '5432'
```

2. Установите зависимости и выполните скрипт `create_tables.py`:

```bash
pip install -r requirements.txt
python3 create_tables.py
```

После успешного выполнения скрипта вы увидите сообщение:

```bash
Database 'validation' created successfully!
```

3. База данных создана. Теперь подключитесь к ней и импортируйте данные из CSV-файлов, расположенных в папке `database/table`, с помощью pgAdmin4 или DBeaver. Для этого нажмите правой кнопкой мыши на таблице и выберите пункт «Импорт данных».

**Важно!** Соблюдайте следующий порядок импортирования таблиц, чтобы избежать ошибок:

1. `mtype`  
2. `stype`  
3. `suppliers`  
4. `material_suppliers`  
5. `materials`  
