# Spring Boot + Postgres (Docker)

Alles starten:

    docker compose up --build

Neue JPA-Klassen: `@Entity`-Klasse in `src/main/java/com/example/demo/model` anlegen
(Tabellen werden per `ddl-auto: update` automatisch erstellt) und ein `JpaRepository` in `repository/`.

Stoppen: `docker compose down` (mit `-v` werden auch die DB-Daten gelöscht).

JUnit-Tests laufen bei `docker compose up --build` automatisch einmal mit (Container `test`, eigene Datenbank `test-db`).
Erneut ausführen: `docker compose run --rm --build test`
