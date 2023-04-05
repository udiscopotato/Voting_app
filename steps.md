1. docker run -d --name redis redis
2. docker run -d --name vote --link redis:redis -p 5000:80 voting-app
3. docker run -d \
    -e POSTGRES_PASSWORD=postgres \
    -e POSTGRES_USER=postgres \
    --name db postgres
          OR
   docker run -d -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres --name db postgres
4. docker build -t worker-app .
5. docker build -t result-app .
6. docker run -d --name worker --link redis:redis --link db:db worker-app
7. docker run -d --name result -p 5001:80 --link db:db result-app
