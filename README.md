# Ideia geral
![image](https://user-images.githubusercontent.com/74191924/208155133-8930e160-8626-4ee1-a897-b4cd6e030a91.png)

# Criar imagem web
```sh
docker build -t monorepo-web . -f Dockerfile-web
```

# Validar as dependências (Não deve ter axios)
```
docker run -it monorepo-web sh
cd node_modules
ls
```

# Criar imagem consumer
```sh
docker build -t monorepo-consumer . -f Dockerfile-consumer
```

# Validar as dependências (Não deve ter express)
```
docker run -it monorepo-consumer sh
cd node_modules
ls
```

# Referências
https://daveiscoding.com/nodejs-typescript-monorepo-via-npm-workspaces

https://raulgf92-software.medium.com/npm-workspaces-microservices-6a13454937ab
