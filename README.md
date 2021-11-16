# .NetCore_MicroServico_Docker
Implementação usando .Net Core 5 e Docker

1. Criar o projeto via terminal
   dotnet new webapi -o NetCoreMicroservico --no-https
   * --no-https = Sem https

2. Acessar na pasta do projeto 
   cd NetCoreMicroservico

3. Iniciar o projeto 
   dotnet run 

4. Acessar projeto no browser ( verificar o numero da porta )
   http://localhost:5000/WeatherForecast

5. Criando Docker 
   * Docker é um container para executação de uma aplicação de forma isolada, ele facilita a implementação uma vez que suas dependencias ficam isoladas não    
     havendo problemas de compatibilidade com outros ambientes dentro de um mesmo servidor.    
     Registry - É um repositório de imagens onde podemos obter nossos modelos para implementação de nossas aplicações. ( DockerHub ) 
     Host     - A partir da imagem criamos o container ( o que seria uma instancia da imagem )
     Client   - Acesso ao container via linha de comando

     * Criar uma conta e baixar o docker em http://docker.com
       Apos instalação teste : docker --version ou docker run hello-world

     5.1 Criar o arquivo Dockerfile com as instruções ( Usar Notepad no VSCode dá erro de execução cl)
     5.2 docker build -t netcoremicroservicodev .
     5.3 docker container run -it --rm -p 3000:80 --name netcoremicroservicodevcont netcoremicroservicodev
     5.4 acessar a aplicação em http://localhost:3000/WeatherForecast

