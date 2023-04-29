# Docker and K8s Questions&Anwsers

## Docker <image src="https://user-images.githubusercontent.com/12403699/227597435-511fd8ae-c873-4fa4-b06f-a6fbe9bc1667.png" width="100" height="80">

1. Você precisa que a imagem **nginx** com a tag **latest** esteja disponível em seu armazenamento local do docker. Você decide baixar esta imagem de um repositório público padrão. Qual comando você deve usar?
   
   - A. docker download nginx:latest
   - B. docker pull nginx:latest
   - C. docker push nginx:latest
   - D. docker get nginx:latest
    
2. Para investigar um problema, você precisa executar um shell interativo (bash) em um contêiner em execução chamado **mycontainer**. Qual comando permitirá que você faça isso de dentro dele?  
   
   - A. docker ssh mycontainer
   - B. docker run -it mycontainer /bin/bash
   - C. docker exec -it mycontainer /bin/bash
   - D. docker exec -d my container --interactive /bin/bash
   
3. Um usuário relatou que o serviço Docker Swarm **billing-manager** parou de funcionar corretamente. Seu cluster ainda está usando os drivers de log padrão. Qual comando você deve usar para coletar informações para fins de Troubleshooting? 
   
   - A. docker service logs billing-manager
   - B. docker swarm logs billing-manager
   - C. docker logs billing-manager
   - D. docker container logs billing-manager
 
4. É possível buildar uma imagem e aplicar tag em vários repositórios em um único comando? 
   
   - A. Sim, pode usar: "docker build \
                        -t example/mynodejs:1.0.3, my-company-registry.com/example/mynodejs:latest"
   - B. Sim, pode usar: "docker build \
                        -t example/mynodejs:1.0.3, \
                        -t my-company-registry.com/example/mynodejs:latest"
   - C. Não, precisa dar build na imagem multiplas vezes com tags diferentes.                       
   - D. Não, precisa dar build na imagem uma única vez e aplicar os tags diferentes.

5. As instruções **COPY** e **ADD** podem ser usadas em um dockerfile para copiar um arquivo para o container durante a fase de build, porém há alguma diferença entre essas instruções?
   
   - A. **COPY** não tem extração *tar* e recursos de manipulação remota de URL, enquanto **ADD** tem.
   - B. **ADD não suporta cópia recursiva, enquanto **COPY** suporta.
   - C. **ADD** não tem extração *tar* e recursos de manipulação remota de URL, enquanto **COPY** tem.
   - D. Não há diferença. **COPY** é um *alias* para **ADD**.
   - E.  **COPY** não suporta cópia recursiva, enquanto **ADD** suporta.
   
 # Kubernetes <image src="https://user-images.githubusercontent.com/12403699/227604690-54fb4263-a38a-4cd5-a4dc-951b19861625.png" width="80" height="80">
  
