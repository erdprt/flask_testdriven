docker-compose -f docker-compose-dev.yml up -d --build
docker-compose -f docker-compose-dev.yml run users python manage.py recreate_db
docker-compose -f docker-compose-dev.yml run users python manage.py test

docker-compose -f docker-compose-dev.yml run users python manage.py cov
docker-compose -f docker-compose-dev.yml run users flake8 project


