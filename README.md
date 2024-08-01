# Dockerfile otimizado para nestjs

Nesse repositório temos 3 opções de dockerfile para usar com projetos nestjs.

[Opção 1](./Dockerfile-1)

Dockerfile simples, somente buildar o projeto e executar.

[Opção 2](./Dockerfile-2)

Dockerfile com dois estágios, no primeiro copia tudo e builda, no segundo copia os arquivos da build e os package*.json e instala as dependencias novamente

[Opção 3](./Dockerfile-3)

Dockerfile utiliza um multi-stage build para criar uma imagem de produção otimizada. A etapa de desenvolvimento é usada para instalar dependências e construir a aplicação. A etapa de build cria o artefato final (dist) e otimiza a imagem. A etapa de produção contém apenas o necessário para executar a aplicação.

## Resultados

| REPOSITORY | TAG    | IMAGE ID     | CREATED          | SIZE |
|------------|--------|--------------|------------------|------|
| nestjs3    | latest | 207b4e43ccf4 | 5 seconds ago    | 142MB|
| nestjs2    | latest | 2b874cbcfa26 | 14 seconds ago   | 144MB|
| nestjs1    | latest | 66d9d10293cc | 32 seconds ago   | 631MB|
