# Leve & Pay

API de integração com o sistema de pagamentos e controle de entregas da Leve & Pay.

# Por onde começar

O primeiro passar para integração é criar um aplicativo no Leve & Pay

> Configurações > Aplicativos

Basta dar um nome ao aplicativo e selecionar um usuário, esse usuário será o usuário
que estaria fazendo as requisições.

# Endereço da API

Todas as requisições deverão ser feitas nas seguintes urls:

```
Homologação/Testes:
https://api.levepay.fun

Produção:
https://api.levepay.com.br
```


# Autenticação

A autenticação é feita pelo `App ID` e `App Secret` que você recebe quando criar o aplicativo,
e deverá ser passado no `header` em todas as requisições.

```
X-APP-ID: App ID
X-APP-SECRET: App secret
```

# Organização

Em todas as requisições também é necessário informar em qual organização está sendo feita
a requisição, para isto basta passar um terceiro `header` também em todas as requisições.

```
X-ORGANIZATION: demo
```

No caso a organização é o que identifica sua empresa, é pode ser encontrada no endereço
que você usa para acessar o sistema.

> https://demo.levepay.com.br

No exemplo acima a organização é `demo`

# Endereços (Endpoints)

## `/transactions/waiting` (GET)

Retorna todas as transações com status `Aguardando pagamento`

## `transactions/:uuid/detail` (GET)

Como o
