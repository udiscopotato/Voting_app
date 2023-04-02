# Voting_app
simple pet voting 3tier web app hosted using docker compose and nginx reverse proxy (reference dockersamples)


services used : 1. flask (python web app for voting frontend)
                2. redis (in-memory cache used to store response from voting frontend and store them in database)
                3. postgres sql (stores votes)
                4. dot.NET (worker node which will do all computation and store our data from redis to db)
                5. node (result site which will take data from DB and show it in result website)
