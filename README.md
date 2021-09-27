# FastAPI-sample-app
- FAST API, PostgreSQL, pgAdmin, docker-compose를 이용한 REST API 구축
- Create Pizza `POST /pizza`
    1. Request

        ```bash
        curl -X 'POST' \
          'http://{IP Address}:8000/pizza/' \
          -H 'accept: application/json' \
          -H 'Content-Type: application/json' \
          -d '{
          "name": "Goguma Pizza",
          "price": 15000,
          "is_cheese_stuffed": true
        }'
        ```

    2. Response

        ```bash
        {"pizza_id":1}
        ```

- Get Pizza `GET /pizza/{id}`
    1. Request

        ```bash
        curl -X 'GET' \
          'http://{IP Address}:8000/pizza/{id}' \
          -H 'accept: application/json'
        ```

    2. Response

        ```bash
        {"name":"Goguma Pizza","price":15000,"is_cheese_stuffed":true}
        ```
