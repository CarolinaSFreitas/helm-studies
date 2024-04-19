# Helm Studies - KodeKloud

https://helm.sh/docs/intro/quickstart/

O Helm é uma ferramenta para Kubernetes que facilita a instalação e o gerenciamento de aplicativos. Ele funciona usando algo chamado "charts", que são basicamente modelos pré-definidos de configuração de aplicativos.

Em vez de você ter que configurar manualmente cada parte do seu aplicativo no Kubernetes, como os serviços, os pods, os volumes, etc., você pode usar um chart do Helm. Esse chart já contém todas as configurações necessárias para implantar o aplicativo de forma consistente e eficiente.

Por exemplo, se você quiser implantar um banco de dados MySQL no Kubernetes, em vez de criar todos os recursos do zero, você pode simplesmente usar um chart do Helm para o MySQL. O chart já terá as definições de configuração prontas para uso, então tudo que você precisa fazer é especificar alguns detalhes específicos do seu ambiente, como o nome do banco de dados e a senha.

O Helm também facilita a atualização e o gerenciamento de versões dos seus aplicativos. Se você precisar fazer uma atualização, basta modificar o chart ou usar comandos do Helm para aplicar as mudanças necessárias, e o Helm cuidará de implantar essas atualizações no seu cluster Kubernetes de forma segura e controlada.

Resumindo, o Helm simplifica o processo de implantação e gerenciamento de aplicativos no Kubernetes, fornecendo modelos pré-definidos de configuração (charts) que podem ser facilmente personalizados e atualizados conforme necessário.

## Comandos do Helm:

- `` helm install <wordpress> ``
- `` helm upgrade <wordpress> ``
- `` helm rollback <wordpress> ``
- `` helm uninstall <wordpress> ``

# Instalação do Helm:

https://helm.sh/docs/intro/install/

Antes de tudo, precisamos já ter um cluster K8s funcional e o kubcetl instalado e configurado com as informações de login prontas.

**Ubuntu/Debian:**
`` curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm ``

ou:

**Windows:**
`` choco install kubernetes-helm ``

Pra conferir a instalação, `` helm version `` ou simplesmente `` helm ``. `` helm `` também vai trazer os comandos que podem ser usados.

![image](https://github.com/CarolinaSFreitas/helm-studies/assets/99994934/48aa10b4-4553-472f-97cb-d056f5114731)

# Usando o ``helm``
Com o ``helm`` podem ser vistas as ações mais comuns pro Helm, variáveis de ambiente, flags, configurações e comandos disponíveis. 

## Ações comuns do Helm:
- `` helm search ``:    search for charts
- `` helm pull ``:      download a chart to your local directory to view
- `` helm install ``:   upload the chart to Kubernetes
- `` helm list ``:      list releases of charts



