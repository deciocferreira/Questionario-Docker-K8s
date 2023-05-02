# Questionário Docker e K8s 

As respostas certas estão destacadas em negrito.

## Docker <image src="https://user-images.githubusercontent.com/12403699/227597435-511fd8ae-c873-4fa4-b06f-a6fbe9bc1667.png" width="100" height="80">

1. Você precisa que a imagem **nginx** com a tag **latest** esteja disponível em seu armazenamento local do docker. Você decide baixar esta imagem de um repositório público padrão. Qual comando você deve usar?
   
   - A. docker download nginx:latest
   - **B. docker pull nginx:latest**
   - C. docker push nginx:latest
   - D. docker get nginx:latest
    
2. Para investigar um problema, você precisa executar um shell interativo (bash) em um container em execução chamado **mycontainer**. Qual comando permitirá que você faça isso de dentro dele?  
   
   - A. docker ssh mycontainer
   - B. docker run -it mycontainer /bin/bash
   - **C. docker exec -it mycontainer /bin/bash**
   - D. docker exec -d my container --interactive /bin/bash
   
3. Um usuário relatou que o serviço Docker Swarm **billing-manager** parou de funcionar corretamente. Seu cluster ainda está usando os drivers de log padrão. Qual comando você deve usar para coletar informações para fins de Troubleshooting? 
   
   - **A. docker service logs billing-manager**
   - B. docker swarm logs billing-manager
   - C. docker logs billing-manager
   - D. docker container logs billing-manager
 
4. É possível buildar uma imagem e aplicar tag em vários repositórios em um único comando? 
   
   - **A. Sim, pode usar: "docker build \
                        -t example/mynodejs:1.0.3, my-company-registry.com/example/mynodejs:latest"**
   - B. Sim, pode usar: "docker build \
                        -t example/mynodejs:1.0.3, \
                        -t my-company-registry.com/example/mynodejs:latest"
   - C. Não, precisa dar build na imagem multiplas vezes com tags diferentes.                       
   - D. Não, precisa dar build na imagem uma única vez e aplicar os tags diferentes.

5. As instruções **COPY** e **ADD** podem ser usadas em um dockerfile para copiar um arquivo para o container durante a fase de build, porém há alguma diferença entre essas instruções?
   
   - **A. **COPY** não tem extração *tar* e recursos de manipulação remota de URL, enquanto **ADD** tem.**
   - B. **ADD** não suporta cópia recursiva, enquanto **COPY** suporta.
   - C. **ADD** não tem extração *tar* e recursos de manipulação remota de URL, enquanto **COPY** tem.
   - D. Não há diferença. **COPY** é um *alias* para **ADD**.
   - E.  **COPY** não suporta cópia recursiva, enquanto **ADD** suporta.
   
6. Considere o seguinte inspect output no Docker:

   <image src="https://user-images.githubusercontent.com/12403699/235465588-775dfe0e-02b2-43ba-901a-0934bbe5d8ed.png" width="600" height="400">
   <image src="https://user-images.githubusercontent.com/12403699/235465664-3b647675-7393-4255-b814-161cf5d21145.png" width="600" height="400">   

   Qual comando deve ser executado para retornar apenas o endereço IP **ipaddress** do container **mycontainer**?

   - **A. docker inspect -f '{{.NetworkingSettings.IPAddress}}' mycontainer**
   - B. docker inspect -f '{{NetworkingSettings(IPAddress)}' mycontainer }
   - C. docker inspect -o mycontainer -o '{{range.NetworkingSettings.Networks}}{{.IPAddress}}{{end}}'
   - D. docker inspect -o '{{mycontainer.NetworkSettings.IPAdress}}'
  
7. Você deseja remover todas a imagens sem uso do seu Docker host para ganhar mais espaço. Qual comando deve executar?
 
    - **A. docker image prune**
    - B. docker rmi --all --unused
    - C. docker system flush image
    - D. docker image rm --all --unused
   
 8. Um *app* chamado **dashboard** baseado na imagem **nginx:latest** precisa ser executado no diretório **/var/www/html/**. Esse diretório é montado em um volume denominado **web_dir** dentro do container. Qual comando deve-se utlizar para esta finalidade?
   
    - A. docker run --name dashboard \
         -v /var/www/html:web_dir nginx:latest
         
    - B. docker run --name dashboard \
         -v web_dir nginx:latest**
      
    - C. docker run --name dashboard \
         -v web_dir:/var/www/html nginx:latest
         
    - D. docker run --name dashboard \
         -v /var/www/html nginx:latest      
         
9. Qual é o diretório **root default** do docker em um sistema Linux? Escreva o diretório completo por extenso.


10. Qual dos comandos a seguir cria um container com um **endereço DNS customizado 8.8.8.8** ?
    
    - A. docker container create -add-dns=8.8.8.8
    - B. docker container create -custom-dns=8.8.8.8
    - C. docker container create -resolve=8.8.8.8
    - D. docker container create -dns=8.8.8.8
    
11. Para aumentar a eficiência e performance do *build* no docker você precisa **excluir arquivos e diretórios irrelevantes** do diretório contexto. O que deve ser feito?
    
    - A. Adicionar o arquivo **.gitexclude** na pasta do contexto para especificar os arquivos irrelevantes files/dirs.
    - D. Usar a opção **docker build -e <irrelevant files/dir> enquanto ocorre o build.
    - C. Usar o instrução **EXCLUDE <irrelevant files/dir> dentro do dockerfile.
    - D. Adicionar o arquivo **.dockerignore** na pasta do contexto para especificar os arquivos irrelevantes files/dirs.
            
   
 # Kubernetes <image src="https://user-images.githubusercontent.com/12403699/227604690-54fb4263-a38a-4cd5-a4dc-951b19861625.png" width="80" height="80">
 
 1. Em qual *namespace* o K8s cria os obejtos internos? Escreva o nome do Namespace completo por extenso.
 
 2. O que deve acontecer quando é executado o seguinte comando? " kubectl scale --current-replicas=2 --replicas=3 deployment/mysql"
    
    - A. Se o deployment denominado **mysql** for configurado para escala 2, ele será escalado para 3.
    - B. O deployment denominado **mysql** será escalado para 2 e terá o autoscaling configurado para no máximo 3 replicas.
    - C. O deployment denominado **mysql** será escalado para 3 não importa como.
    - D. O deployment denominado **mysql** será escalado para 2 não importa como.
    
3. Qual dos seguintes recursos do K8s pode ser usado para fazer o **host-based routing** para múltiplas aplicações rodando dentro do cluster?

   - A. IngressController
   - B. Ingress
   - C. Serviço do tipo LoadBalancer
   - D. Não há como fazer essa configuração. Há apenas como fazer rotamento **path-based** 
   
4. Queremos executar aplicações no K8s que carrega um grande arquivo de dados após a inicialização e apenas aceita requisições de entrada depois de completar a carga dos dados. Qual *probe* deve ser usado para ter a certeza de que as requisições para os pods até aquele ponto?   

   - A. pingProbe
   - B. readinessProbe
   - C. livenessProbe
   - D. startupProbe
 
5. No K8s, um *Probe* é um diagnóstico feito periodicamente pelo *kubelet* em um container. Para performar, o *kubelet* invoca um *handler* implementado pelo container. Qual das opções a seguir de *handler* não é suportado pelo K8s?
 
   - A. UDPSocketAction
   - B. TCPSockerAction
   - C. ExecAction
   - D. HTTPGetAction
