# PostgreSQL Docker Compose Setup

This repository contains a Docker Compose configuration for setting up PostgreSQL with pgAdmin and automated backups.

## Features

- PostgreSQL latest version with optimized configuration
- pgAdmin for database management
- Automated backups

- Pre-configured server connection in pgAdmin
- Performance tuning
- Volume mapping for data persistence

## Directory Structure

```
.
├── docker-compose.yml    # Main Docker Compose configuration
├── .env                  # Environment variables
├── pg_configs/           # PostgreSQL custom configurations
│   └── custom-postgres.conf

├── pgadmin-servers.json  # Pre-configured server for pgAdmin
└── README.md             # This file
```

## Getting Started

1. Create the required directories:

```bash
mkdir -p D:/DOCKER/POSTGRESQL_VOLUME/{data,pgadmin,backups}
mkdir -p ./pg_configs

```

2. Modify the `.env` file to set your credentials and configurations.

3. Start the containers:

```bash
docker compose up -d
```

4. Access pgAdmin:
   - URL: http://localhost:5050
   - Email: admin@example.com (or your configured email)
   - Password: pgadmin_password (or your configured password)

## PostgreSQL Connection Details

- Host: localhost (from host) or postgres (from other containers)
- Port: 5432 (or your configured port)
- Username: postgres (or your configured username)
- Password: your_secure_password (or your configured password)
- Database: postgres (or your configured database)

## Backup Information

Backups are automatically performed based on the schedule configured in the `.env` file and stored in the `D:/DOCKER/POSTGRESQL_VOLUME/backups` directory.

## Custom Configuration

You can modify the PostgreSQL configuration by editing the `pg_configs/custom-postgres.conf` file.



## License

This project is open-source and free to use.