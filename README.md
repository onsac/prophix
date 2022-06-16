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
## Certificado Configurado
<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/Keyclock_Certificados_Configurados.jpeg" >
</p>

## Configurando prophix gateway como serviço
```sh
sudo su - phgtw

pm2 start /opt/prophix-gtw/prophix-gtw/prophix-gtw.js

pm2 startup

sudo env PATH=$PATH:/opt/prophix-gtw/.nvm/versions/node/v11.15.0/bin /opt/prophix-gtw/.nvm/versions/node/v11.15.0/lib/node_modules/pm2/bin/pm2 startup systemd -u phgtw --hp /opt/prophix-gtw

exit

sudo systemctl enable pm2-phgtw

sudo systemctl start pm2-phgtw
```
## Serviço Configurado

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/Keyclock_Servi%C3%A7o_Configurado.jpeg" >
</p>

## Solicitação para configuração do Identity Provider (Integração do Keycloak Prophix com Keycloak Sebrae)

<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/Keyclok_Solicita%C3%A7%C3%A3o_para_configura%C3%A7%C3%A3o_do_Identity_Provider.jpeg" >
</p>

>Enviar arquivo keycloak-prophix-broker-openid-configuration.json para TOTVS

## Configuração do Client (Integração com Keycloak Sebrae)
<p align="center">
     <img src="https://github.com/onsac/prophix/blob/main/Imagens/Keycloy_Configura%C3%A7%C3%A3o_%20do_Client.jpeg" >
</p>

>Enviar o Client ID e Secret para TOTVS
