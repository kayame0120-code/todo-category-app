# laravel-docker-template

## 環境構築

```bash
docker compose up -d --build
docker compose exec php composer install
docker compose exec php cp .env.example .env
docker compose exec php php artisan key:generate
docker compose exec php php artisan migrate --seed
```

- アプリ: http://localhost:8051
- `.env` と `vendor/` はリポジトリに含めていません（上の手順で作られます）
