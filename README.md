build the project     :     docker-compose -f docker-compose-dev.yml up -d --build
build and create db   :     docker-compose -f docker-compose-dev.yml run users python manage.py recreate_db
build and test        :     docker-compose -f docker-compose-dev.yml run users python manage.py test
build and coverage    :     docker-compose -f docker-compose-dev.yml run users python manage.py cov
build and lint        :     docker-compose -f docker-compose-dev.yml run users flake8 project


