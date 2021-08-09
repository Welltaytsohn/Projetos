Resultado: https://app.powerbi.com/view?r=eyJrIjoiMWIxNDI3MDYtNDY4Mi00ZjJjLTlmMjItMTBmZTFmNDI4NTA4IiwidCI6ImJkNWFhZjZiLTU1ZDUtNDgwOS05OWUyLTA2N2E3YTczZWUxMCJ9

O objetivo do Case é prever qual time o usuário torce, baseado em seu consumo, produtos que possui do Grupo Globo e algumas informações demográficas.
Para isso, montamos uma amostra de usuários e seus consumos no portal do Globo Esporte.
 
Preferencialmente usando R ou Python, você deve desenvolver um ou mais modelos para inferir o time de cada usuário da base. Você pode focar nos principais times do brasil, se julgar necessário.
 
Os bancos são descritos abaixo:
 
·         BD_DEM_TIME: Esse banco contém informações demográficas:
o   KEY: Chave única do usuário;
o   SEXO: Sexo;
o   DTA_NASC: Data de Nascimento. (Ano);
o   ESTADO: Estado;
o   TIMES: Time de futebol do usuário;
 
·         BD_CONSUMO: Esse banco contém informações de consumo no portal do Globo Esporte:
o   KEY: Chave única do usuário;
o   tempo: Tempo que o usuário ficou na página (url);
o   url: Página que o usuário visitou;
 
·         BD_SERVICOS: Esse banco contém informações da lista de serviços, ou seja, é um banco que contém quais produtos o usuário possui:
o   KEY: Chave única do usuário;
o   GLOBOPLAY: 1 se possui o produto e 0 caso contrário;
o   PREMIERE_PLAY: 1 se possui o produto e 0 caso contrário;
o   GLOBOSAT_PLAY: 1 se possui o produto e 0 caso contrário;
o   COMBATE: 1 se possui o produto e 0 caso contrário;
o   CARTOLA_PRO: 1 se possui o produto e 0 caso contrário;
 
Algumas observações sobre a variável “URL”
- Essa variável indica qual a página que o usuário acessou.
- No portal do globoesporte.com existem editorias de time são da seguinte forma:
TIME 1 – a url contem a seguinte estrutura ‘/time1/’
Ex.:
Por Time:
Flamengo – ‘/flamengo/’
  Exemplo de url: ‘https://globoesporte.globo.com/futebol/times/flamengo/noticia/fla-volta-ao-rio-pressionado-e-diego-discute-com-torcedores-rodinei-e-hostilizado.ghtml’
Por Campeonato:
Copa do Brasil – ‘/copa-do-brasil/’
  Exemplo de url: ‘https://globoesporte.globo.com/futebol/copa-do-brasil/noticia/cbf-realiza-sorteio-das-semifinais-da-copa-do-brasil-nesta-quarta-feira.ghtml’