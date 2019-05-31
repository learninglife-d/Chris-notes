# Fix
## Error: laravel.log could not be opened.

```
sudo chown -R nginx:nginx storage/
sudo chown -R nginx:nginx storage/logs
sudo chown -R nginx:nginx bootstrap/cache
sudo chmod -R 775 storage/
sudo chmod -R 775 storage/logs/
sudo chmod -R 775 bootstrap/cache/

sestatus
setenforce Permissive
sudo setenforce 0
```