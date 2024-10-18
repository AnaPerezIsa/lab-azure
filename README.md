# lab-azure
Crie uma VM com um Template 
Neste passo a passo, implantaremos uma máquina virtual com um modelo QuickStart e examinaremos os recursos de monitoramento.

Tarefa 1: Explore a galeria QuickStart e localize um modelo
Nesta tarefa, navegaremos pela galeria do Azure QuickStart, acessaremos o repositório GitHub do Azure QuickStart e implantaremos um modelo que cria uma máquina virtual.

Entre no portal do Azure: https://portal.azure.com

No ambiente de laboratório, abra uma nova janela do navegador e insira https://azure.microsoft.com/en-us/resources/templates/?azure-portal=true . Na galeria, você encontrará vários modelos populares e atualizados recentemente. Esses modelos automatizam a implantação de recursos do Azure, incluindo a instalação de pacotes de software populares. Navegue pelos muitos tipos diferentes de modelos disponíveis.

Abra uma nova aba ou janela do navegador e insira https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.compute/vm-simple-windows para acessar a página Implantar um modelo simples de VM do Windows no repositório do Azure QuickStart GitHub. Observe que esse repositório hospeda uma grande variedade de fontes de modelo.

Role para baixo na página Implantar um modelo de VM simples do Windows e clique no botão Implantar no Azure . Sua sessão do navegador será redirecionada automaticamente para o portal do Azure .

Observação : O botão Deploy to Azure permite que você implante o modelo por meio do portal do Azure. Durante essa implantação, você será solicitado apenas a fornecer um pequeno conjunto de parâmetros de configuração.

Quando solicitado, entre na sua assinatura do Azure usando as credenciais fornecidas anteriormente nas instruções.

Clique em Editar modelo . O formato do modelo do Resource Manager usa o formato JSON. Revise os parâmetros e variáveis. Em seguida, localize o parâmetro para o nome da máquina virtual. Altere o nome para myVMTemplate . Salve suas alterações.

Captura de tela do modelo com a alteração do nome da VM em destaque.

Agora configure os parâmetros requeridos pelo template (substitua xxxx no prefixo do rótulo DNS por letras e dígitos de forma que o rótulo seja globalmente único). Deixe os padrões para todo o resto.

Contexto	Valor
Inscrição	Manter padrão fornecido
Grupo de recursos	Use o padrão fornecido no menu suspenso
Região	Manter padrão
Tamanho da VM	Padrão_D2s_v3
Nome de usuário do administrador	usuário azure
senha do administrador	Pa$$w0rd1234
Prefixo de rótulo DNS	meumodelovmxxxx
Versão do SO	2019-datacenter-segundo-geração
Clique em Revisar + Criar .

Monitore sua implantação.

Tarefa 2: verificar e monitorar a implantação da sua máquina virtual
Nesta tarefa, verificaremos se a máquina virtual foi implantada corretamente.

Na lâmina Todos os serviços , procure e selecione Máquinas virtuais .

Certifique-se de que sua nova máquina virtual foi criada.

Captura de tela da página de máquinas virtuais. A nova VM é mostrada e está em execução.

Selecione sua máquina virtual e, no painel Visão geral , selecione a guia Monitoramento e role para baixo para visualizar os dados de monitoramento.

Observação : o período de monitoramento pode ser ajustado de uma hora a 30 dias.

Revise os diferentes gráficos fornecidos, incluindo CPU (média) , Rede (total) e Bytes de disco (total) .

Captura de tela dos gráficos de monitoramento da máquina virtual.

Clique em qualquer gráfico. Note que você pode Adicionar métrica e alterar o tipo de gráfico.

Retornar para a lâmina Visão geral . (deslize a barra de alternância para a esquerda)

Clique no Activity log (painel esquerdo). Os Activity logs registram eventos como criação ou modificação de recursos.

Clique em Adicionar filtro e experimente pesquisar diferentes tipos de eventos e operações.

Captura de tela da página Adicionar filtros com o tipo de evento selecionado.

Parabéns! Você criou com sucesso um recurso a partir de um modelo e implantou esse modelo no Azure.

