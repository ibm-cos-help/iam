---

copyright:
  years: 2018
lastupdated: "2018-11-30"

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Obtendo um token do {{site.data.keyword.Bluemix_notm}} IAM usando uma chave API
{: #iamtoken_from_apikey}

As APIs do {{site.data.keyword.Bluemix}} podem ser acessadas somente pelos usuários que estão autorizados por uma função de IAM designada. Portanto, o usuário que está chamando a API deve passar credenciais para a API autenticar. É possível gerar um token do IAM usando a sua [chave de API do {{site.data.keyword.Bluemix_notm}}](/docs/iam/userid_keys.html#userapikey) ou uma [chave de API do ID do serviço](/docs/iam/serviceid_keys.html#serviceidapikeys). Este processo também será usado se você estiver desenvolvendo um aplicativo que precisa trabalhar com outros serviços do {{site.data.keyword.Bluemix_notm}}. Deve-se usar uma chave API do ID de serviço para obter um token de acesso para ser passado para cada um dos serviços do {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}

1. Use o comando `curl` a seguir para gerar um token do IAM usando uma chave API.

### POST /identity/token

### Cabeçalhos
  - Content-Type: application/x-www-form-urlencoded
  - Accept: application/json

### Parâmetros
  - grant_type=urn:ibm:params:oauth:grant-type:apikey
  - apikey=*[Api key]*

```
curl -k -X POST \
  --header "Content-Type: application/x-www-form-urlencoded" \
  --header "Accept: application/json" \
  --data-urlencode "grant_type=urn:ibm:params:oauth:grant-type:apikey" \
  --data-urlencode "apikey=<apikey>" \
  "https://iam.bluemix.net/identity/token"
```
{: codeblock}

A amostra a seguir é a resposta esperada:

### Resposta

```
{
  "access_token": "eyJhbGciOiJIUz......sgrKIi8hdFs",
  "refresh_token": "SPrXw5tBE3......KBQ+luWQVY=",
  "token_type": "Bearer",
  "expires_in": 3600,
  "expiration": 1473188353
}
```
{: codeblock}
