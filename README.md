<p align="center">
  <a href="https://onsac.com/">
    <img src="https://github.com/onsac/prophix/blob/main/Imagens/AIO-KEYCLOAK.png" >
  </a>
</p>

<h3 align="center">AIO Keycloak</h3>

<p align="center">
  Documentação AIO Keycloak
  <br>
  <a href="https://onsac.com/"><strong>Conheça mais sobre nosso serviço »</strong></a>
  </p>
 


## Topologia

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/1%20-%20Topologia.jpeg" >
</p>

## Prophix-Broker

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/2%20-%20Prophix-Broker.jpeg" >
</p>

## Client prophix-gtw

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/3%20-%20Client%20prophix-gtw.jpeg" >
</p>

## Sebrae - Identity Provider

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/4%20-%20Sebrae%20-%20Identity%20Provider.jpeg" >
</p>

## AD Local

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/5%20-%20AD%20Local.jpeg" >
</p>

## Usuários sincronizados

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/6%20-%20Usu%C3%A1rios%20sincronizados.jpeg" >
</p>

## Login (prophix-gtw)

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/7%20-%20Login%20(prophix-gtw).jpeg" >
</p>

## Redirect para url (obs.: podemos configurar qualquer url)

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/8%20-%20Redirect%20para%20url%20(obs%20podemos%20configurar%20qualquer%20url).jpeg" >
</p>

##  Informações do usuário no keycloak

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/9%20-%20Informa%C3%A7%C3%B5es%20do%20usu%C3%A1rio%20no%20keycloak.jpeg" >
</p>

## prophix-gtw

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/10%20-%20prophix-gtw.jpeg" >
</p>

## prophix-gtw + AD Local

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/11%20-%20prophix-gtw%20%2B%20AD%20Local.jpeg" >
</p>

## Usuário sincronizado com AD Local

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/12%20-%20AD%20Local.jpeg" >
</p>

## Configuração do Certificado

To convert a PFX file to separate public and private key PEM files:
Extracts the private key form a PFX to a PEM file:
```sh
openssl pkcs12 -in filename.pfx -nocerts -out key.pem
```
Exports the certificate (includes the public key only):
```sh
openssl pkcs12 -in filename.pfx -clcerts -nokeys -out cert.pem
```
Removes the password (paraphrase) from the extracted private key (optional):
```sh
openssl rsa -in key.pem -out server.key
```
## Certificados Configurados
<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/Keyclock_Certificados_Configurados.jpeg" >
</p>
