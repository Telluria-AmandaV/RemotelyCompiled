# RemotelyCompiled
Os arquivos estão disponíveis na release, onde a fonte é o repositório Remotely
As adaptações se resumem à configurações de acesso para que os instaladores e executáveis já estejam previamente configurados para utilização
Demais informações sobre a aplicação disponíveis na descrição da release

Repositório com a adaptação: https://github.com/Telluria-AmandaV/Remotely
Repositório original da aplicação: https://github.com/lucent-sea/remotely

## Detalhes do Processo de Adaptação:
A principal modificação foi realizada no arquivo Publish.ps1. Nele, foi adicionada a configuração do sistema operacional, o endereço do host e o endereço para a compilação do arquivo. O ID da organização utilizado na página de instalação foi configurado no código fonte da aplicação, mais precisamente nas propriedades do arquivo AgentInstaller -> MainWindow.xaml. Existe na aplicação um outro endereço de host e um GUID para ID, que são utilizados na aplicação padrão para debug. 

A compilação foi feita utilizando o Powershell do Windows, assim como recomendado pelo desenvolvedor original do Remotely. Caso seja necessário refazer a compilação, o Windows pode travar a execução do script devido à configurações de segurança. O comando "Set-ExecutionPolicy Unrestricted", executado em modo de administrador no Powershell, desativa este filtro de segurança. Confirme escolhendo a opção sim[s]. Para reverter, basta digitar "Set-ExecutionPolicy Restricted" e confirmar escolhendo a mesma opção do processo anterior.
