ELASTICSEARCH VJEZBA

Pokretanje

Pokretanje Elasticsearch i Kibana:
docker compose up -d

Kibana:
http://localhost:5601

OPIS:
U ovoj vježbi sam:
- pokrenula Elasticsearch i Kibanu pomoću Dockera
- kreirala indeks "knjige"
- ubacila podatke pomoću Bulk API-ja
- radila različite upite (match, term, range, bool)
- koristila analyzer
- radila agregacije
- napravila vlastiti indeks "filmovi"

STRUKTURA:
- docker-compose.yml 
- queries.json 
- ODGOVORI.md 
- screenshots/ 