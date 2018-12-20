Ensure `db/postgres_data` folder is present both in `.gitignore` and `.dockerignore` files since it embbeds PostgreSQL container's data (to persist them between containers recreations)
