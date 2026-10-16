# DISCLAIMER

Esse repositório é composto pelo material produzido durante o estudo de Django e o acompanhamento das aulas presentes no canal do YouTube de Jefferson Lobatto. O código aqui pode não refletir o que está presente nas aulas originais. E não me compromento em manter o conteúdo fiel ao apresentado lá. 

Esse conteúdo está sendo mantido duranto o aprendizado aplicado e pode ser exxluído (ou tornado privado) a qualquer momento. 

O conteúdo original do Jefferson Lobatto está aqui[https://github.com/JeffersonLobato/curso_django]. Ele não possuí arquivo de licença vinculado, então este aqui não também não terá.

Caso queira ver os videos das aulas do Jefferson Lobato segue link para a playlist[https://www.youtube.com/playlist?list=PLLVddSbilcumgeyk0z6ko5U_FYPfbRO2C] do YouTube dele. Tenha em mente que os videos tem três anos de idade (na data desse commit (15/10/2026)).  


# Curso de Django
A partir daqui teremos a documentação dos elementos apresentados no projeto, em decorrência da progressão das aulas. A estutura desse repositõrio NÃO seguirá a estrutura de uma pasta por aula. serã apenas um projeto que receberá commits conforme eu for avançando nas aulas, e ao final deve ficar APENAS o projeto completo. 

## Aula 1 - Resumo
Criação do ambiente virtual para gerencimaneto de versão de pacotes:

    $ python -m venv ll_env

 Instalação do pacote Django no python:

    (ll_env) $ pip install Django
    
Criação do projeto no formato Django: 

    (ll_env) $ django-amdin startproject learning_log .
    
    ##### O "." faz com que o Django não crie uma nova pasta apenas para o projeto. <br>
    ##### Ele cria o projeto direto na pasta que você está usando no terminal.

Não houve alterações das configurações iniciais. Então rodou se o *migrate* e o *runserver* direto: <br>
    
    (ll_env) $ python manage.py migrate
    
    # Esperado um retorno similar ao abaixo:

        Operations to perform:
            Apply all migrations: admin, auth, contenttypes, sessions
        Running migrations:
            Applying contenttypes.0001_initial... OK
            Applying auth.0001_initial... OK
            Applying admin.0001_initial... OK
            Applying admin.0002_logentry_remove_auto_add... OK
            Applying admin.0003_logentry_add_action_flag_choices... OK
            Applying contenttypes.0002_remove_content_type_name... OK
            Applying auth.0002_alter_permission_name_max_length... OK
            Applying auth.0003_alter_user_email_max_length... OK
            Applying auth.0004_alter_user_username_opts... OK
            Applying auth.0005_alter_user_last_login_null... OK
            Applying auth.0006_require_contenttypes_0002... OK
            Applying auth.0007_alter_validators_add_error_messages... OK
            Applying auth.0008_alter_user_username_max_length... OK
            Applying auth.0009_alter_user_last_name_max_length... OK
            Applying auth.0010_alter_group_name_max_length... OK
            Applying auth.0011_update_proxy_permissions... OK
            Applying auth.0012_alter_user_first_name_max_length... OK
            Applying sessions.0001_initial... OK


    (ll_env) $ python manage.py runserver
    
    # Esperado um retorno similar ao abaixo:

        Watching for file changes with StatReloader
        Performing system checks...

        System check identified no issues (0 silenced).
        October 16, 2026 - 00:01:33
        Django version 5.2, using settings 'learning_log.settings'
        Starting development server at http://127.0.0.1:8000/
        Quit the server with CONTROL-C.

        WARNING: This is a development server. Do not use it in a production setting. Use a production WSGI or ASGI server instead.
        For more information on production servers see: https://docs.djangoproject.com/en/5.2/howto/deployment/