# Ferramentas de Implantação no Azure

## Passo 1: Acessar o Azure Cloud Shell
Abrir o Azure Cloud Shell

Acesse portal.azure.com.
No canto superior direito do portal, clique no ícone do Cloud Shell (um terminal com um símbolo de maior).
Escolher o Tipo de Shell

Selecione entre Bash (Azure CLI) e PowerShell (Azure PowerShell).

## Passo 2: Área de Automação no Azure
O que é a Área de Automação?

A Área de Automação do Azure fornece uma plataforma para automatizar processos e tarefas com o uso de Runbooks, Process Automation, e Configuration Management.
Criar uma Conta de Automação

No portal do Azure, procure e selecione “Automation Accounts”.
Clique em “+ Criar”.
Preencha os detalhes obrigatórios, como Nome, Assinatura, e Grupo de Recursos.
Escolha a Localização e clique em “Revisar + Criar” e depois em “Criar”.
Criar e Executar um Runbook

Navegue até sua conta de automação.
No menu à esquerda, selecione “Runbooks” e clique em “+ Criar um Runbook”.
Dê um nome ao Runbook, selecione o tipo de Runbook (por exemplo, PowerShell ou Python), e clique em “Criar”.
Edite o Runbook e adicione o código necessário para a automação.
Clique em “Publicar” e depois em “Iniciar” para executar o Runbook.

## Passo 3: Usar Azure Bicep
O que é Azure Bicep?

Azure Bicep é uma linguagem de infraestrutura como código que simplifica a criação de templates do Azure Resource Manager (ARM). Ela fornece uma sintaxe mais limpa e legível comparada ao JSON.
Criar um Arquivo Bicep

No Cloud Shell, crie um arquivo Bicep usando um editor de texto:
nano main.bicep
Adicione o código Bicep. 
Implantar o Arquivo Bicep

Execute o comando abaixo para implantar o template Bicep:
az deployment group create --resource-group <nome-do-grupo> --template-file main.bicep
Verificar a Implantação

Use o comando para verificar o status da implantação:
az deployment group show --resource-group <nome-do-grupo> --name <nome-da-implantação>

## Passo 4: Usar Azure Arc
O que é o Azure Arc?

Azure Arc permite que você gerencie recursos fora do Azure, como servidores on-premises e clusters Kubernetes, usando a plataforma do Azure. Ele estende o gerenciamento e governança do Azure para recursos em ambientes híbridos e multi-cloud.
Adicionar Servidor ao Azure Arc

No portal do Azure, vá para “Azure Arc” e selecione “Servidores”.
Clique em “+ Adicionar”.
Siga as instruções para instalar o agente do Azure Arc no servidor que deseja adicionar. Geralmente envolve baixar e executar um script no servidor.
Adicionar um Cluster Kubernetes ao Azure Arc

Vá para “Azure Arc” e selecione “Kubernetes clusters”.
Clique em “+ Adicionar” e siga as instruções para conectar seu cluster Kubernetes.
Isso geralmente envolve a instalação do Azure CLI e a execução de comandos específicos para registrar o cluster com o Azure Arc.
Gerenciar Recursos com Azure Arc

Após adicionar recursos ao Azure Arc, você pode gerenciá-los no portal do Azure como se fossem recursos do Azure nativos.
Use os menus para aplicar políticas, visualizar logs, e configurar alertas para seus recursos conectados via Azure Arc.
