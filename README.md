# SISTEMA DE AUTENTICAÇÃO EM DJANGO

## VERSÃO PYTHON UTILIZADA NO PROJETO
- python 3.9.7

## REQUERIMENTOS DO PROJETO
- Instale o [virtualenv aqui](https://virtualenv.pypa.io/en/latest/installation.html)
- Comando para instalação através do pip - ``pip install virtualenv``
## INICIANDO O PROJETO
- Antes de rodar os comandos, certifique-se de estar na pasta raíz do projeto.
- Crie uma virtualenv - ``virtualenv venv``
- Ative a virtualenv - ``.\venv\Scripts\activate
- Instalando dependências - ``pip install -r requirements.txt``.
- Rodando aplicação - ``python .\login_service\manage.py runserver``.
## ROTAS
- '/' - Rota principal que apresenta a documentação da API através do Swagger.

## TODAS AS ROTAS PARA MANUSEIO DE CONTA
- accounts/ signup/ [name='account_signup']
- accounts/ login/ [name='account_login']
- accounts/ logout/ [name='account_logout']
- accounts/ password/change/ [name='account_change_password']
- accounts/ password/set/ [name='account_set_password']
- accounts/ inactive/ [name='account_inactive']
- accounts/ email/ [name='account_email']
- accounts/ confirm-email/ [name='account_email_verification_sent']
- accounts/ ^confirm-email/(?P<key>[-:\w]+)/$ [name='account_confirm_email']
- accounts/ password/reset/ [name='account_reset_password']
- accounts/ password/reset/done/ [name='account_reset_password_done']
- accounts/ ^password/reset/key/(?P<uidb36>[0-9A-Za-z]+)-(?P<key>.+)/$ [name='account_reset_password_from_key']
- accounts/ password/reset/key/done/ [name='account_reset_password_from_key_done']
- accounts/ social/

## BIBLIOTECAS UTILIZADAS
- drf-yasg [Yet another Swagger generator] - ``https://drf-yasg.readthedocs.io/en/stable/readme.html``
- django-rest-auth - ``https://django-allauth.readthedocs.io/en/latest/installation.html``
