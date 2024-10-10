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
