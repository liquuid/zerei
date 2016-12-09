# Zerei

Sistema de registro de jogos 

## Como desenvolver?

1. clone o repositório
2. crie o virtualenv com python 3.5
3. ative o virtualenv.
4. instale as dependencias.
5. configure a instancia com o .env
6. execute os testes

```console
git clone git@github.com:liquuid/zerei.git
cd zerei
python -m venv .venv
source .zerei/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test
```

## Como fazer deploy

1. Crie uma instancia no heroku
2. Envie as configurações para o heroku
3. Defina uma SECRET_KEY segura para a instancia
4. Defina DEBUG=False
5. Configure o serviço de email.
6. Envie o código para o heroku

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# configuro o email
git push heroku master --force
```

[![Build Status](https://travis-ci.org/liquuid/zerei.svg?branch=master)](https://travis-ci.org/liquuid/wttd-eventex)
[![Code Health](https://landscape.io/github/liquuid/zerei/master/landscape.svg?style=flat)](https://landscape.io/github/liquuid/wttd-eventex/master)
[![Coverage Status](https://coveralls.io/repos/github/liquuid/zerei/badge.svg?branch=master)](https://coveralls.io/github/liquuid/wttd-eventex?branch=master)
