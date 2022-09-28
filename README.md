Reading mbtiles metadata:

```bash
sqlite3 poland-bicycle-infra.mbtiles
```

```SQL
select * from metadata where name is not 'json';
```
