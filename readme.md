<img src="https://github.githubassets.com/assets/actions-matrix-aac8c29bd225.svg" min-width="150px" max-width="150px" width="150px" align="right" alt="">

# URI-QR-GENERATOR.

UMA API HTTP SIMPLES PARA GERAR CÓDIGOS QR DE URI NO FORMATO SVG. BY DEVELOPER DAVIDSONBPE...

----------

### LINK

```bash
https://uri-qr-generator.vercel.app/?uri=https://uri-qr-generator.vercel.app/
```

--------

### GIT CLONE

```bash
git clone https://github.com/redek-dp/uri-qr-generator.git
```

--------

### CD PASTA

```bash
cd uri-qr-generator
```

--------

### NPM INSTALL

```bash
npm install
```

--------

### NODE SERVER

```bash
node index.js
```

--------

SE TUDO ESTIVER FUNCIONANDO CORRETAMENTE, VOCÊ RECEBERÁ A SEGUINTE MENSAGEM:

```
URI-QR-GENERATOR ESTÁ AGUARDANDO CONEXÕES NA PORTA 8225
```

## CONFIGURAÇÃO

CASO ESTEJAM DEFINIDAS, UTILIZAMOS AS SEGUINTES VARIÁVEIS ​​DE AMBIENTE:

| VARIÁVEL   | CONFIGURAÇÃO                                                         | PADRÃO  |
|------------|----------------------------------------------------------------------|---------|
| PORT       | PORTA EM QUE O SERVIDOR HTTP DEVE ESCUTAR. | `8225`  |
| PARAM_NAME | NOME DO PARÂMETRO `GET` QUE CONTÉM A URI A SER CODIFICADA EM QR CODE. | `URI`   |
| URI_PREFIX | PREFIXO A SER ADICIONADO AO INÍCIO DE TODAS AS URIS.                 | *VAZIO* |

## USO

FAÇA UMA REQUISIÇÃO `HTTP GET` PARA `HTTPS://SERVER:PORT/?URI=HTTPS://00020126450014BR.GOV.BCB.PIX01`. A RESPOSTA É UM QR CODE NO FORMATO SVG. ESSA É A REPRESENTAÇÃO EM QR CODE DA URI `HTTPS://00020126450014BR.GOV.BCB.PIX01`.

LEMBRE-SE DE CODIFICAR CORRETAMENTE OS PARÂMETROS DA REQUISIÇÃO `GET`.

### INCORPORANDO QR CODES COMO IMAGENS HTML

COMO ESTAMOS UTILIZANDO PARÂMETROS `GET`, PODEMOS USAR A URI DA REQUISIÇÃO COMO FONTE DA IMAGEM, A QUAL PODERÁ SER ARMAZENADA EM CACHE POR NAVEGADORES, PROXIES, ETC.

SE O PARÂMETRO `PORT` ESTIVER DEFINIDO COMO `80` (A PORTA HTTP PADRÃO DOS NAVEGADORES), VOCÊ PODE OMITIR A PORTA AO UTILIZAR AS IMAGENS.

`<img src="https://server/?uri=https://00020126450014BR.GOV.BCB.PIX01" alt="https://00020126450014BR.GOV.BCB.PIX01" />`

### CONFIGURAÇÃO DE PROTEÇÃO CONTRA ABUSO

A MENOS QUE VOCÊ PROTEJA SUA API (POR EXEMPLO, UTILIZANDO UM PROXY ATRAVÉS DE OUTRO SERVIDOR HTTP), QUALQUER PESSOA QUE FIZER REQUISIÇÕES AO SEU SERVIÇO PODERÁ GERAR CÓDIGOS QR GRATUITAMENTE UTILIZANDO SEUS RECURSOS.

UM CASO DE USO TÍPICO É A GERAÇÃO DE CÓDIGOS QR PARA UM ÚNICO NOME DE DOMÍNIO. DEFINA SUA VARIÁVEL **URI_PREFIX** COMO `"HTTPS://MY-DOMAIN"` E, EM SEGUIDA, PASSE URLS RELATIVAS NOS VALORES DOS PARÂMETROS `GET`. COMO TODO CÓDIGO QR COMEÇARÁ COM O SEU NOME DE DOMÍNIO, O SERVIÇO NÃO TERÁ UTILIDADE PARA TERCEIROS.

VOCÊ TAMBÉM DEVE RENOMEAR O PARÂMETRO `GET` PARA `PATH`, TORNANDO AS REQUISIÇÕES DA API MAIS CLARAS:

AGORA, `HTTP://SERVER:PORT/?PATH=/A/B` RETORNARÁ UM CÓDIGO QR NO FORMATO SVG, APONTANDO PARA `HTTPS://MY-DOMAIN/A/B`

## SOLUÇÃO DE PROBLEMAS

CERTIFIQUE-SE DE QUE A PORTA HTTP (*PADRÃO: 8225*) NÃO ESTEJA SENDO UTILIZADA POR OUTRO PROCESSO E/OU ALTERE A PORTA HTTP NA CONFIGURAÇÃO. EM ALGUNS SISTEMAS OPERACIONAIS, NÃO É POSSÍVEL ESCUTAR EM PORTAS INFERIORES A 1000 SEM PRIVILÉGIOS DE ROOT.

--------

<br />

## CONECTE-SE COM NÓS:

[<img height="30" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="davidsonbpe | YouTube" />][youtube]
[<img height="30" src="https://img.shields.io/badge/Twitter-222?style=for-the-badge&logo=x&logoColor=white" alt="davidsonbpe | Twitter" />][twitter]
[<img height="30" src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="davidsonbpe | Instagram" />][instagram]
[<img height="30" src="https://img.shields.io/badge/CodePen-003333?style=for-the-badge&logo=c&logoColor=white" alt="davidsonbpe | CodePen" />][CodePen]
[<img height="30" src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="davidsonbpe | Facebook" />][facebook]
[<img height="30" src="https://img.shields.io/badge/GitHub-003333?style=for-the-badge&logo=github&logoColor=white" alt="davidsonbpe | GitHub" />][github]
<a href="mailto:dev7.capital366@passinbox.com" alt="Email">
<img height="30" src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=Minutemailer&logoColor=white" /></a>
<a href="https://br.pinterest.com/davidsonbpe/" alt="Pinterest">
<img height="30" src="https://img.shields.io/badge/Pinterest-FF0000?style=for-the-badge&logo=Pinterest&logoColor=white" /></a>

<br />

<a href="https://dav7.pages.dev/" align="right" alt="Visitor count">
<img height="30" src="https://raw.githubusercontent.com/davserv/d-framework/refs/heads/img-iso/count.svg" /></a>

<br />


[twitter]: https://twitter.com/davidsonbpe
[youtube]: https://www.youtube.com/channel/UCHqvw9v2Fp6o006lUskoigg/
[instagram]: https://www.instagram.com/davidsonbpe/
[facebook]: https://www.facebook.com/decomrradio/
[CodePen]: https://codepen.io/davidsonbpe/
[github]: https://github.com/davidsonbpe/


