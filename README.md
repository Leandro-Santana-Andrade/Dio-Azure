# Resumo Dio-Azure
Repositório de resumo do estudo sobre cloud Azure.

# MODULO 1 <h6>
   - Introducao ao ambiente cloud:
      Foi mostrados os tipos de servicos e os direitos e deveres da fornecedor do servico e cliente.
      
   - Como criar uma conta para uso do Azure:
     Demonstra os passos para criacao da conta e cuidados ao utilizar as funcionalidades.
   
   - Mostra os principais beneficios da nuvem: 
         Confiabilidade: O sistema funciona com risco minimo de falhas.
         Previsibilidade: Planejar uma configuracao de forma antecipada.
         Segurança: Protecao contra acesso interno e externo sem permissao. 
         Escalabilidade: Adiciona desempenho conforme necessario.
         Elasticidade: O sistema se adequa aos recursos solicictados.
   
   - O modulo descreve os tipos de servico disponiveis no ambiente de nuvem.
      * IaaS: Infra estrutura como servico. Nesse modelo, a fornecedora fica responsavel por entregar o hadware e a rede. O restante fica por responsabiliade do cliente.
      * PaaS: Plataforma como servico. O forncedor, sobe o nivel de servico entrega e disponibiliza um ambiente pronto para o cliente.
      * SaaS: No software como servico, geralmente é a nivel de aplicacao, onde o cliente possui o menor nivel de responsabilidade. 

# MODULO 2 <h6>
- Regiões: locais no globo onde possui data center da nuvem, atualmente possui 60 regiões. A região deve ter pelo menos 3 data centers por região. Toda região possui uma região par para o caso de desastre. Regiões soberanas são regiões que possui acesso restrito para determinado cliente, geralmente órgão governamental. 

- Recursos:
	* Maquinas virtuais
	* Contas de armazenamento
	* Redes virtuais
	* Serviços de aplicativos
	* Bancos de dados
	* Funções

- Assinatura:
	Utiliza o sistema 1:n, nesse modelo, uma conta pode possuir varias assinaturas. Dessa forma, é possível modularizar o projeto por equipes. Também permite ter um controle maior, permitindo uma segurança maior no ambiente.

- Disponibilidade de Maquinas Virtual
	É uma boa pratica criar grupos de maquinas virtuais para manter a disponibilidade de uma sistema ou serviço.

- Sistema remotos, contêineres e aplicativos:
	Área de trabalho remota: maquinas virtualizadas que permitem acesso de forma remota para realizar uma tarefa ou utilizar um serviço. 
	Contêineres: gestão de serviços sem a necessidade de gastar recursos com um sistema operacional, dessa forma torna o consumo de hardware mais eficiente.
	Aplicativos de Função: serviço que permite gerar um código sem a necessidade de criar uma infraestrutura completa para gerenciar/utilizar a aplicação.

- Armazenamento
	 Conta de armazenamento: conta deve possuir nome exclusivo dentro de toda a rede e pode receber diversos tipos de dados, dentre eles: 
		* blobs: feito para armazenar dados não estruturados
		* discos: fornece discos para vm, aplicativos e serviços utilizarem.
		* filas:  serviço de armazenamento de mensagens
		* files: compartilhamento de arquivos na rede com alta disponibilidade. 
		* Tabelas: fornece uma opção de chave para armazenamento de dados estruturados não relacionais.  

- Redundância de armazenamento: 
     LRS: redundância local
     ZRS: redundância de zona
     GRS: redundância geográfica
     GZRS: redundância zona geográfica

- Camadas de acesso

	* Frequente: dados acessados com frequência
	* Esporádico: dados acessados com pouca frequência, intervalo de 30 dias entre as consultas.
	* Frio: dados acessados com pouca frequência, intervalo de 90 dias entre as consultas. 
	* Arquivo morto: raramente acessado, intervalo de pelo menos 180 dias entre as consultas.

- Migrações de Dados para Azure
  
	* Azure Data Disc: equipamento para transferencia de dados com ate 40 tera.
	* Azure Data Box: equipamento para transgênicos de dados, 1 equipamento pode transporta até 80 tera de dados.
	* Azure Data Heavy: projetado para transferir mais de 800 tera de dados.
	* AzCopy:
		- Utiliza linhas de comandos .
		- Copia arquivos da conta na nuvem.
		- Sincronização unidirecional.
		- Indicado para quantidade baixa ou mediana de dados.

  	* Gerenciamento de Armazenamento Azure:
		- Utiliza ambiente gráfico para gerenciamento de dados.
		- Compatível com diversos sistemas operacionais.
		- Sincronização de arquivos do Azure.
		- Sincronização bidirecional.
		- Utiliza cache, acesso a arquivo local.
  
 - Identidade, Acesso e segurança

   * Entra ID: serviço de gerenciamento de identidade, permitindo um login único (SSO) acessar a nuvem.

   * Autenticação X autorização
     - Autenticação: o usuário existe e foi validado para acessar o serviço.
     - Autorização: nível de acesso que o usuário possui dentro do sistema.

   * MFA (autenticação multifator) :
     - Algo que você sabe ( usuário e senha )
     - Algo que voce possui (equipamentos)
     - Algo que você é ( biometria ) 

   * Autenticação b2b ( identidade externa ): traz uma identidade de fora do serviço para acessar o ambiente específico como convidado.
     
   * Autenticação b2c ( business to custumer ): compartilha recurso com usuário de autenticação externa.
     
   * Acesso condicional: ferramenta para permitir/ negar acesso a recursos através de sinais.:
     - Associação de usuários / grupo
     - Local de IP
     - Dispositivo 
     - Aplicativo 
     - Detecção de risco

   * Controle de acesso baseado em função ( RBAC )
     - Gerenciamento de acesso de granulação fina
     - Conceder somente a quantidade mínima de acesso
     - Habilitar controle de acesso aos recursos 

   * Modelo de confiança zero: sempre conseder acesso mínimo ao recursos. Uma abordagem em camadas para proteger o sistema.

     Camadas de proteção completa: 
        - Segurança física 
        - Identidade e acesso 
        - Perímetro 
        - Rede 
        - Computação 
        - Aplicativo 
        - Dados 

# MODULO 3 <h6>

Gerenciamento de custo: O tipo de recurso define o custo sobre o serviço, assim como a categoria também afeta o custo final.

* Modelos de consumo:

	* Pagar conforme o uso. 
	* Reserva, onde predefine um período de uso de serviço.

* Manutenção: monitorar seu ambiente permite validar se o custo sobre aquele serviço ainda é necessário. Consequentemente esse controle pode gerar uma redução de custo.
* Área geográfica: dependendo do local o mesmo serviço pode ter um custo diferente.
* Trafego de rede: Enviar dados para o nuvem pode ser gratuito, dependendo do cenário. Porem, o trafego de dados entre recursos pode ser afetado por zonas de cobrança. 
* Assinatura: o tipo de assinatura afeta o custo. 
* Azure Marketplace: Ambiente onde é possível adquirir licença de softwares, implantação de aplicativos, ferramentas para desenvolvimento entre outros produtos. Caso esse item apresente problema, o suporte da aplicação deve ser acionado, a Azure não é responsável por essa função.

Calculadora de custo e preços: ferramenta que ajuda a ter uma estimativa do custo sobre o serviço. Para esse calculo, são validados os seguintes fatores:

   - Região
   - Camada
   - Opção de cobrança
   - Opção de suporte
   - Programa e ofertas
   - Preço de desenvolvimento/teste doa Azure

TCO(Calculadora de custo total de propriedade): Ferramenta para estimar a economia de custos possível ao migrar para nuvem. 

Relatório de comparação dos custos das infraestruturas locais com os custos de uso de serviço na nuvem. 

Marcas: Organiza e fornece metadados aos recursos do Azure, porem, não são obrigatórios ou herdados. Muito útil para reunir informações de cobrança.


* Governança e conformidade 
	
	- Azure Policy: ajuda a impor padrões e avaliar a conformidade. A policy ignora qualquer permissão aplicada a um usuário. 

	- Bloqueio de recursos: Protege recursos no Azure de exclusão ou modificação acidental. Esse serviço permite gerenciar bloqueios na assinatura, grupo de recursos ou níveis de recursos individuais dentro do Portal Azure. As configurações de bloqueio são herdáveis. 
	
	Tipos de bloqueio:
		- Exclusão: Permite ler, permite atualizar e não permite excluir um serviço/recurso
		- Somente Leitura: Permite ler, não permite atualizar e não permite exclusão de recursos/serviço.

	Obs.: Caso o recurso seja movido e a regra de bloqueio não foi diretamento atribuido a ele, não migrado com ele a regra de bloqueio de exclusão.

* Portal de Confiança do Serviço: Onde pode identificar regras e protocolos para atendimento a tipos de empresas e/ou governos. 

* Microsoft Purview: Serve para gerenciamento de governança, risco e conformidade de dados. Fornece um relatório de como os  dados estão sendo tratados na base local, nuvem ou software como serviço. 

* Portal de Confiança do Serviço: onde pode identificar regras e protocolos para atendimento a tipos de empresas e/ou governos. 

* Microsoft Purview: serve para gerenciamento de governança, risco e conformidade de dados. Fornece um relatório de como os  dados estão sendo tratados na base local, nuvem ou software como serviço. 


* Ferramentas de implantação de recursos.

    * Portal Azure: responsável por gerenciar e criar recursos no Azure.
    * Azure PowerShell e CLI: terminal para interagir via liha de comando.
    * Azure Arc: serviço responsável por gerenciar recursos que estão fora da cloud. 
    * Azure Resource Manager (ARM): fornece uma camada de gerenciamento que permite criar, atualizar e exclusão de recursos no Azure.
       
	![image](https://github.com/user-attachments/assets/d22c5498-23e8-4f3b-b7b4-e95e8e91d207)

* Infraestrutura como código
    * Garanta consistência na implantação em todo o ecossistema de nuvem
    * Gerencie a configuração em escala
    * Provisionar rapidamente o ambiente com infraestrutura pre pronta.

* Modelos de ARM: São arquivos em JSON que podem ser usados para criar e implantar a infraestrutura sem a necessidade de criar comandos.

* Bicep: modelo de linguagem específica de domínio (DSL) para automatisar o ambiente.

* Ferramentas de Monitoramento.
    * Assistente do Azure(Advisor): ajuda a analisar recursos e faz recomendações baseados em boas praticas para otimizar as implantações no Azure. Esse serviço valida os seguintes tópicos: 
        * Confiabilidade
        * Segurança
        * Desempenho
        * Custo
        * Excelencia operacional
    * Integridade do serviço: coleção de serviços que mantem o usuário informado sobre o status geral do Azure, de serviços ou recursos. 
    * Status do Azure: visão global da integridade de todos os servicos em todas as regiões do Azure
    * Resource Health: exibição personalizada dos recursos reais do Azure. Fornece informações sobre a integridade de recursos individualmente.
    * Azure Monitor: maximiza a disponibilidade e o desempenho de aplicativos coletando, analisando e tomando decisões com base na telemetria da nuvem e de ambientes.
