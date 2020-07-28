# upload-file-graphql  
Poc em Node JS com TypeScript para fazer upload de arquivo com GraphQL  
  
## npm i  
  
Será necessário baixar todas as dependências do projeto, para isso use o comando **npm i** dentro da pasta do projeto  
  
## Executando o projeto  
  
Execute o comando: **npm run start**  
O servidor é executado na porta **7411**  
Para parar: **Ctrl + c**  
  
## Exemplo de solicitações com Insominia  
  
1. Clique em **New request**  
2. Escolha um nome e tipo de solicitação **POST**  
3. Para o corpo, escolha **MuitpartForm**  
4. Na URL, use: **http://localhost:7411/**  
5. Na guia Multipart, use os parâmetros:  
- **operations**, escolha o tipo Texto (várias linhas) com o conteúdo:  
{  
  "query":"mutation fileUpload($file: Upload!) {\n fileUpload(file: $file)\n}",  
  "variables":{ "file": null},  
  "operationName":"fileUpload"  
}  
- **map**, escolha o tipo de texto com o conteúdo: value: **{"file": ["variables.file"]}**  
- **file**, escolha o tipo de arquivo e selecione um arquivo na máquina local  
6. Clique no botão **Enviar** e você verá a guia Visualizar com o retorno.  
  
## Dependências  
### ts-node-dev  
Ele reinicia o processo do nó de destino quando qualquer um dos arquivos necessários é alterado (como padrão node-dev), mas compartilha o processo de compilação Typcript entre as reinicializações. Isso aumenta significativamente a velocidade de reiniciar comparando com node-dev -r ts-node/register ..., nodemon -x ts-node ...variações, porque não há necessidade de instanciar ts-nodecompilação de cada vez.  
  
Instalação: **yarn add ts-node-dev --dev** ou **npm i ts-node-dev --save-dev**  
Link para referência: https://www.npmjs.com/package/ts-node-dev  
 
### typescript  
TypeScript é uma linguagem para JavaScript em escala de aplicativo. O TypeScript adiciona tipos opcionais ao JavaScript que suportam ferramentas para aplicativos JavaScript em grande escala para qualquer navegador, host ou sistema operacional. O TypeScript é compilado para JavaScript legível, baseado em padrões. Experimente no parquinho e mantenha-se atualizado através do nosso blog e conta no Twitter.  
  
Instalação: **npm install -g typescript**  
Link de referência: https://www.npmjs.com/package/typescript  
  
    

