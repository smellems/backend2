## Testing
Run all unit tests using

    python manage.py test

## Background tasks
All background tasks are managed by [Celery](http://www.celeryproject.org/). To start running a (development) worker process use:

    celery -A pleio worker -l info

## Full-text index
For full-text indexing Pleio relies on [Elasticsearch](https://www.elastic.co/). To re-index the full database run the command:

    python manage.py rebuild_index

## Frontend
The frontend assets are managed by Webpack. First make sure you downloaded [Node.js v8](https://nodejs.org/en/download/) and [yarn](https://yarnpkg.com/en/docs/install). To download all the assets run:

    yarn install

For developing use:

    yarn run watch

this will boot up a watch server with hot-reloading capabilities. To build a production version of the assets run:

    yarn run build

## Documentation
The documentation is managed by [docute.js](https://docute.js.org/). To view the documentation locally first install docute:

    yarn global add docute-cli

Then preview the docs using:

    docute ./docs
