# Pdf-Challenge
### Este repositorio tem como objectivo partilhar diferentes implementações de librarias de pdf, em tecnologias e linguagens diferentes.

## Como participar?
Cria uma branch seguindo o padrão *(nome)-(tecnologia)-(libraria)*, exemplos:
* eriksongm-csharp-questpdf
* cage-php-blocoecimento

## Como implementar?
O teu projecto deve implementar uma interface Swagger com um metodo POST com nome do template, que recebe os dados a serem renderizados no PDF, a modo que cada request, vai gerar um PDF com os dados enviados no mesmo.

### Rotas dos Endpoints
![image](https://user-images.githubusercontent.com/11561779/226875299-d6e569da-f641-4688-904f-d32c898987b8.png)

### Conteudo do request
![image](https://user-images.githubusercontent.com/11561779/226875445-7d6a9be9-c116-4c72-86d4-c63b814d6276.png)

```
{
  "companyName": "string",
  "companyAddress": "string",
  "clientName": "string",
  "clientAddress": "string",
  "items": [
    {
      "quantity": 99999,
      "description": "string",
      "price": 999999999
    }
  ],
  "invoiceNumber": "string",
  "date": "2023-03-22T10:27:37.571Z",
  "po": "string",
  "dueDate": "2023-03-22T10:27:37.571Z"
}
```
### chamada via CURL
```
curl -X 'POST' \
  'http://localhost:5000/Invoice/Invoice1' \
  -H 'accept: */*' \
  -H 'Content-Type: application/json' \
  -d '{
  "companyName": "string",
  "companyAddress": "string",
  "clientName": "string",
  "clientAddress": "string",
  "items": [
    {
      "quantity": 99999,
      "description": "string",
      "price": 999999999
    }
  ],
  "invoiceNumber": "string",
  "date": "2023-03-22T10:30:28.013Z",
  "po": "string",
  "dueDate": "2023-03-22T10:30:28.013Z"
}'
```

## Modo de publicação
O projecto deve contar com um ficheiro dockerfile, que deve permitir criar uma imagem docker, esta imagem vai ser publicada no dockerhub facilitando assim os testes dentro da comunidade.

Qualquer outra informação relativa a execução da imagem, deve ser documentada no ficheiro readme incluido na tua branch.

## Que template devo utilizar no PDF?
Lista de templates:
### Invoice1
![image](https://user-images.githubusercontent.com/11561779/226834430-f21a4d59-7f68-4635-a995-b5aa1e7d321d.png)
### Invoice2
![image](https://user-images.githubusercontent.com/11561779/226834496-2e117189-f1fb-4bce-91f6-43abfab2d29c.png)
### Invoice3
![image](https://user-images.githubusercontent.com/11561779/226834562-b1d84e5f-50ae-4b6f-a99d-b192c0124c79.png)
### Invoice4
![image](https://user-images.githubusercontent.com/11561779/226834617-a4f09fb6-8b34-4a69-8852-5380a1fe173e.png)

# Não sabe programar, não complica.
