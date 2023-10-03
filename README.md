# Mastodon Docker Compose

```
git clone --recursive <repo>
```

```
docker compose run --rm web test
```

```
docker compose exec -it db su postgres -c 'psql'
```

```sql
CREATE USER mastodon CREATEDB;
ALTER ROLE mastodon LOGIN password '<YOUR_PASSWORD>';

\q
```

change `.env.production`
```
docker compose run --rm web bundle exec rake mastodon:setup
```

change `ssl_certificate` `ssl_certificate_key`
`data/nginx/mastodon.conf`

```
docker compose up -d
```

TODO:
1. certificate