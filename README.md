
# Sky Stack Konfiguration




## Kør lokalt

Denne stack kører følgende applikationer
- Skyboard (frontend)
- SkySensorsAPI (API)
- PostgreSQL (database)

### Docker Installation

For at køre dette projekt skal du have Docker installeret på dit system. Følg disse trin for at installere Docker:

1. Gå til [Docker-hjemmesiden](https://www.docker.com/products/docker-desktop) og download Docker Desktop til dit operativsystem.
2. Følg installationsinstruktionerne fra Docker for at fuldføre installationen.

### Kørsel af Docker Compose-filen

Når Docker er installeret, følg disse trin for at køre Docker Compose-filen:

1. Klon dette repository til din lokale maskine:

```
git clone https://github.com/SkySensors/SkyStack
```

2. Naviger til projektets mappe


3. Tilføj en .env fil med følgende variabler
    ```
    DB_PASS=
    DB_NAME=
    DB_USERNAME=
    ```


4. Kør Docker Compose:
```
docker-compose --env-file ./.env up
```

Denne kommando vil bygge de nødvendige Docker-billeder og starte de containere, der er defineret i `docker-compose.yml`-filen. 
- Skyboard på `http://localhost:80`.
- SkySensorsAPI `http://localhost:8080`

### Andre Docker Compose kommandoer
- Det er muligt at ændre database password udfra "POSTGRES_PASSWORD"
- For at stoppe Docker Compose, brug følgende kommando:
```
docker-compose down
```