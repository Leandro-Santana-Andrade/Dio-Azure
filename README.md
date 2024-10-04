# Dio-Azure
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
