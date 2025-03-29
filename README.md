<h1 align="center"> BANP - BECOME A NEW PERSON </h1>
<p align="center">Um trabalho para a disciplina de DESENVOLVIMENTO DE APLICAÇÕES PARA DISPOSITIVOS MÓVEIS - 4º Informática do IFSP-Jacareí</p>
<br>
<p align="center">
<img loading="lazy" src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=blue&style=for-the-badge"/>

<h1>🧑‍🏫 Professor responsável</h1> 

-  Carlos Eduardo Duque Polito

<h1>🎯 Objetivo do projeto</h1> 

O BANP (Become a New Person) é um aplicativo de monitoramento de vícios que ajuda os usuários a acompanharem seu progresso na abstinência. O app permite registrar recaídas, visualizar estatísticas sobre o tempo e dinheiro economizados, fazer anotações e acessar artigos sobre saúde mental. Seu principal objetivo é fornecer suporte na jornada de recuperação, ajudando os usuários a desenvolverem maior autoconsciência e controle sobre seus hábitos prejudiciais. 

<br>

<h1>✖️ O que não é o objetivo do projeto</h1>

- Monetização
- Não iremos compartilhar dados para pesquisas, pois nosso foco é a privacidade do usuario

<h1>👥 Público-alvo</h2>
O BANP (Become a New Person) é voltado para pessoas que desejam monitorar e reduzir hábitos prejudiciais, como consumo de álcool, tabagismo, jogos de azar e outros vícios.

<h1>:hammer: Requisitos funcionais do projeto</h1>

- usuarios → Cadastro, login, recuperação de senha, configurações da conta.

- tipos_vicios → Lista de tipos de vícios disponíveis para seleção.

- vicios → Registro de vícios, exibição na tela principal, tempo/dinheiro economizado, remoção de vício.

- recaidas → Registro de recaídas, impacto, duração, anotações, atualização automática dos dados.

- anotações → Registro, exibição e edição de anotações.

- artigos → Exibição e seleção de artigos.

<h1>☑️ Requisitos não funcionais para o site</h1> 

- Desempenho: O software deve funcionar sem travamentos e com agilidade de resposta.
- Segurança: O software deve garantir que os dados do cliente estejam em segurança e que sejam acessados só pelo mesmo.
- Ser desenvolvido para mobile: O software deve ser desenvolvido para Android e IOS. 


<h1>📑 Matrizes de Requisitos</h1>

<h2>Matriz de Requisitos Gerais</h2>


<h2>Matriz de Requisitos Funcionais</h2>
<img width="1059" alt="Captura de Tela 2025-03-28 às 23 05 24" src="https://github.com/user-attachments/assets/dd7d4ff4-601a-435d-ac8d-f3f80638b8c7" />


<h2>Matriz de Requisitos de Sistema</h2>
<img width="1059" alt="Captura de Tela 2025-03-28 às 23 42 46" src="https://github.com/user-attachments/assets/6817d130-15a6-4606-bfa2-36206f0ad069" />

<h1>📱Mockup do APP </h1>

Mockup da Interface: 
![Wireframe de apps](https://github.com/user-attachments/assets/4e746339-d0c5-4afe-8e33-722be8e17995)

[Mockup] (https://github.com/user-attachments/files/19514217/Wireframe.de.apps.2.pdf)



<h1>📊 Modelagem do Banco de Dados</h1>
<img width="1059" alt="Captura de Tela 2025-03-28 às 22 34 55" src="https://github.com/user-attachments/assets/73bcda73-db5f-4c96-9415-75fdc1340b5f" />

<br><br>

<h1>📖 Dicionário de dados </h1>

<h2>Coleção usuários</h2>
Essa coleção é necessária para cadastrar o usuário e seus dados, permitindo autenticação e personalização da conta.
<br><br>

"uid": É um campo do tipo String. "Identificador único do usuário no sistema."

"nome": É um campo do tipo String. "Armazena o nome completo do usuário."

"email": É um campo do tipo String. "Contém o endereço de e-mail do usuário, usado para login."

"created_time": É um campo do tipo Timestamp. "Armazena a data e hora do cadastro do usuário."

<h2>Coleção vicios</h2>
"Essa coleção contém os tipos de vícios que o usuário pode escolher para monitorar, garantindo organização no sistema."
<br><br>

"id": É um campo do tipo String. "Identificador único do tipo de vício."

"nome": É um campo do tipo String. "Armazena o nome do vício (exemplo: 'Álcool', 'Tabagismo')."

"descricao": É um campo do tipo String. "Contém uma breve descrição do vício."

"created_time": É um campo do tipo Timestamp. "Registra a data e hora da criação do tipo de vício."

<h2>SubColeção vicios_do_usuário</h2>
"Essa coleção armazena os vícios que o usuário está monitorando, permitindo o acompanhamento do progresso e recaídas."
<br><br>

"id": É um campo do tipo String. "Identificador único do vício do usuário."

"tipoVicioId": É um campo do tipo String. "Referência ao tipo de vício cadastrado."

"data_inicio": É um campo do tipo Timestamp. "Armazena a data em que o usuário começou a monitorar esse vício."

"tempo_economizado": É um campo do tipo Integer. "Tempo total economizado desde o início da abstinência (em horas)."

"dinheiro_economizado": É um campo do tipo Float. "Valor economizado ao evitar o vício (em moeda local)."

"tempo_total_gasto": É um campo do tipo Integer. "Tempo total gasto no hábito antes do monitoramento (em horas)."

"created_time": É um campo do tipo Timestamp. "Registra a data e hora do registro do vício."

<h2>SubColeção recaidas</h2>
"Essa coleção permite que o usuário registre recaídas, ajudando no autoconhecimento e controle do hábito."
<br><br>

"id": É um campo do tipo String. "Identificador único da recaída."

"data": É um campo do tipo Timestamp. "Armazena a data da recaída."

"hora": É um campo do tipo String. "Contém o horário da recaída."

"duracao": É um campo do tipo Integer. "Tempo gasto no vício durante a recaída (em minutos)."

"impacto": É um campo do tipo String. "Indica o impacto da recaída ('Tempo', 'Dinheiro' ou 'Saúde')."

"anotacao": É um campo do tipo String (opcional). "Armazena um comentário do usuário sobre a recaída."

"created_time": É um campo do tipo Timestamp. "Registra a data e hora do registro da recaída."

<h2>SubColeção Anotações</h2>
"Essa coleção permite que o usuário registre seus sentimentos e reflexões ao longo da recuperação."
<br><br>

""id": É um campo do tipo String. "Identificador único da anotação."

"data": É um campo do tipo Timestamp. "Armazena a data da anotação."

"texto": É um campo do tipo String. "Contém o conteúdo da anotação escrita pelo usuário."

"created_time": É um campo do tipo Timestamp. "Registra a data e hora do registro da anotação."

<h2>SubColeção artigos</h2>
"Essa coleção contém artigos sobre saúde mental e recuperação, oferecendo suporte ao usuário na jornada de mudança de hábitos."
<br><br>

"id": É um campo do tipo String. "Identificador único do artigo."

"titulo": É um campo do tipo String. "Armazena o título do artigo."

"conteudo": É um campo do tipo String. "Contém o texto completo do artigo."

"created_time": É um campo do tipo Timestamp. "Registra a data e hora da publicação do artigo."


<h1>🧍Diagramas UML</h1>

<h2>Diagrama de Componenetes</h2> 
<img width="756" alt="Captura de Tela 2025-03-28 às 23 47 14" src="https://github.com/user-attachments/assets/0831d43b-abcc-4086-8b8c-939f1fe886b8" />




<h2>Diagrama de Caso de uso</h2>
<img width="752" alt="Captura de Tela 2025-03-28 às 23 48 05" src="https://github.com/user-attachments/assets/ce8b0c8a-19d6-4f8a-89a3-2ec026a9edf2" />




<h1> Plano de capacidade (baseado em 1.000 usuários/mês).</h1>

<h2>🛢️ Armazenamento (Firestore)</h2>

- Componente	Estimativa/Mês	Observações
- Coleção users	5 MB/mê. Estimativa: 5 KB por usuário (email, UID, etc.)
- Coleção collections + items	500 MB. Estimativa:	50 coleções/usuário, 10 KB cada
- Total	505 MB	Sem mídia (fotos/vídeos)

<h2>🔐 Autenticação (Firebase Auth)</h2>

- 2.100 operações/mês (logins + cadastros).
  
<h2>⚙️ Processamento (Back-end FlutterFlow)</h2>

- 30.000 requisições (CRUD básico).

<h2>📸 Armazenamento de Mídia (Firebase Storage)</h2>

- 2 GB/mês (10.000 itens com fotos de 200 KB cada).

<h2>⚠️ Limites do Plano Gratuito</h2>

- Firestore: 50K leituras/dia e 20K escritas/dia.
- Auth: 10K usuários/mês.
- Storage: 5GB

<h1>🛡️ Estratégia de Backup e Recuperação</h1>

<h2>1. Objetivo</h2>

- Garantir a integridade e disponibilidade dos dados do sistema, permitindo a recuperação eficiente em caso de falhas, exclusões acidentais ou erros técnicos.

<h2>2. Dados que serão incluídos nos backups</h2>

- Informações dos usuários
- Dados das coleções e itens cadastrados
- Imagens associadas aos itens
- Configurações essenciais do sistema

<h2>3. Ferramentas utilizadas</h2>

- Banco de dados: Firebase Firestore
- Armazenamento de imagens: Firebase Storage 


<h1>🧰 Tecnologias Utilizadas</h1> 

Front-end e back-end:
<br><br>
<img src="https://img.shields.io/badge/FlutterFlow-0256F2?style=for-the-badge&logo=flutter&logoColor=white">
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white">

Banco de Dados:
<br><br>
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white">

