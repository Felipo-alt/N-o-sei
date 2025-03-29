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

<img src="https://github.com/user-attachments/assets/696fb228-1d78-42db-a689-1016e78f84bd" width=1000> 

<br>
- Observação: C.T significa Criação de Tela. É um requisito tanto de back-end quanto de Front-end, pois no Flutterflow o desenvolvimento de ambas das partes são mais unidas por ser low-code.

<h2>Matriz de Requisitos Funcionais</h2>
<img src="https://github.com/user-attachments/assets/59564692-1a81-4232-80c0-3bd26a9ae1d7" width=1000>

<h2>Matriz de Requisitos de Sistema</h2>
<img src="https://github.com/user-attachments/assets/e2229f0f-2851-4360-875f-6b3b9a6d7502" width=1000>

<h1>📱Mockup do APP </h1>

Mockup da Interface:[Mockup](https://github.com/user-attachments/files/19514217/Wireframe.de.apps.2.pdf)



<h1>📊 Modelagem do Banco de Dados</h1>
<img src="https://github.com/user-attachments/assets/1d0b66fd-5ff7-4ea5-874c-063865fb1997" width=1000>

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
"favoritos": É um campo do tipo Array de Strings. "Lista de usuários que favoritaram o artigo."
"created_time": É um campo do tipo Timestamp. "Registra a data e hora da publicação do artigo."


<h1>🧍Diagramas UML</h1>

<h2>Diagrama de Componenetes</h2> 
<img src="https://github.com/user-attachments/assets/76b349ee-d94c-437e-89a6-74c07e4d9922" width=1000>

<h2>Diagrama de Classes<h2>
<img src="https://github.com/user-attachments/assets/e3bebcd1-113d-4aa0-bff0-005b87bd00af" width=1000>

<h2>Diagrama de Caso de uso</h2>
<img src="https://github.com/user-attachments/assets/f9f66082-ec21-4763-af0c-121ddb38ef4e" width=1000>
<h2>Os casos de uso podem ser dividios em:</h2>

- `Fazer cadastro`: Quando acessado pela primeira vez, o aplicativo permite ao usuário criar uma conta. Essa criação de conta envolve o preenchimento de um formulário, onde o usuário deve fornecer o email, senha e confirmar a senha. Após isso, o mesmo será redirecionado para a tela de questionário, onde irá fornecer: Nome, idade, motivo de utilizar o aplicativo e uma foto de perfil.
- `Fazer login`: Quando o usuário já possui uma conta, ele pode acessá-la através de um login. Para isso, é necessário responder um formulário com o email e senha da conta já criada.
- `Logout`: Quando já logado em uma conta, o usuário pode sair dela facilmente. Ele pode fazer essa ação para entar em outra conta, por exemplo.
- `Coleções`: O usuário pode fazer o CRUD (Create, Read, Update, Delete) das coleções, ou seja, o usuário é capaz de criar, visualizar, atualizar e deletar coleções. Seja características da coleção em si, ou os componentes daquela coleção. Além disso, o usuário consegue (por meio de uma barra de pesquisa) buscar, pelo nome, alguma coleção já criada por ele antes. 
- `Itens`:  O usuário pode fazer o CRUD (Create, Read, Update, Delete) dos itens, ou seja, o usuário é capaz de criar, visualizar, atualizar e deletar os itens das coleções. Além disso, o usuário consegue (por meio de uma barra de pesquisa) buscar, pelo nome, algum item de uma coleção específica. 


  
<h2>Diagramas de Sequência</h2>

<p>Tela de Login e Cadastro</p>

<img src="https://github.com/user-attachments/assets/d0f9a5ea-114c-48d8-a86e-3e04cb3b74d4" width=1000>

<p>Tela principal, criação de coleção e criação de item</p>
<img src="https://github.com/user-attachments/assets/35b832b8-e041-4062-a6cc-eb7d8619f55d" width=1000>

<h2>Diagramas de Atividade<h2>
  
<p>Tela de Login e Cadastro</p>
<img src="https://github.com/user-attachments/assets/e8a411ac-a3fb-49ce-8ed9-0d72826935b1" width=1000>
<p>Tela principal, criação de coleção e criação de item</p>
<img src="https://github.com/user-attachments/assets/6f1a476f-ffc7-40da-ae29-cee477a90920" width=1000>

<h2>Diagrama de Objetos</h2>
<img src="https://github.com/user-attachments/assets/77a476e2-8286-4316-9a99-4457930f0042" width=1000>

<h2>Diagrama de Pacotes</h2>
<img src="https://github.com/user-attachments/assets/19d080db-652a-419f-9f5e-3deec4e5fd79" width=1000>

<h2>Diagrama de Implantação</h2>
<img src="https://github.com/user-attachments/assets/6b66e54b-ac1d-4548-ad0d-b268fb845424" width=1000>

<h2>Diagrama de Estrutura Composta</h2>
<img src="https://github.com/user-attachments/assets/ced1766d-d03a-4621-99e4-8410e2bb0fc8" width=1000>

<h2>Diagrama de Perfil</h2>
<img src="https://github.com/user-attachments/assets/c37e9160-4c89-4afa-b466-7b80af410b58" width=1000>

<h2>Diagrama de Comunicação</h2>
<img src="https://github.com/user-attachments/assets/1b039f26-80fe-4e16-8a68-13174970caf9" width=1000>

<h2>Diagrama de Estados</h2>
<img src="https://github.com/user-attachments/assets/40fc6652-9893-4e9a-a8b1-75f5f2e845d4" width=1000>

<h2>Diagrama de Tempo</h2>
<img src="https://github.com/user-attachments/assets/41357a85-2458-4d54-a45e-8617bf8dfea8" width=1000>

## Documentação do Usuário - The Collector

### Introdução

The Collector é um aplicativo projetado para colecionadores organizarem e gerenciarem suas coleções de maneira intuitiva. Este guia fornecerá instruções detalhadas sobre como utilizar todas as funcionalidades do aplicativo.

### Objetivos da Documentação

- Auxiliar os usuários a navegar e utilizar o aplicativo com eficiência.
- Proporcionar uma experiência fluida e satisfatória.
- Capacitar os usuários a resolver problemas de forma independente.

### Guia de Uso

#### 1. Acessando o Aplicativo

##### Tela de Login

Opções:
- Entrar com usuário e senha.
- Continuar com Google ou Apple.
- Opção de redefinir senha.

##### Criar Conta

- Preencha os campos obrigatórios: nome de usuário, senha e confirmação de senha.
- Alternativamente, cadastre-se com Google ou Apple.

#### 2. Criando um Perfil

##### Formulário de Cadastro

- Nome completo.
- Idade (menores de 18 anos são permitidos).
- Motivo para utilizar The Collector.

#### 3. Criando uma Coleção

##### Passos

- Acessar "Criar Coleção"
- Preencher os campos:
  - Nome da coleção (ex: "Cartas Pokémon").
  - Tipo da coleção (ex: "Relógios").
  - Data de início da coleção.
  - Enviar foto representativa.

#### 4. Adicionando Itens à Coleção

##### Passos

- Selecione uma coleção existente.
- Clique em "Adicionar Novo Item".
- Informe os detalhes:
  - Nome do item.
  - Status (novo, usado, raro, etc.).
  - Valor estimado (ex: R$ 400,00).
  - Código do item (se aplicável, ex: 150/200).
  - Quantidade do item.
  - Foto do item.
- Salve as informações.

#### 5. Gerenciando a Coleção

##### Recursos Disponíveis

- Visualizar todas as coleções criadas.
- Editar informações de uma coleção ou item.
- Excluir coleções ou itens indesejados.

#### 6. Configurações da Conta

##### Opções Disponíveis

- Alterar nome de usuário.
- Mudar foto de perfil.
- Modificar senha.
- Ativar/desativar o modo de "Texto para Fala".

#### 7. Resolvendo Problemas Comuns

##### Problema: Não consigo fazer login

- Verifique se o nome de usuário e senha estão corretos.
- Utilize a opção "Esqueci minha senha" para redefinir.

##### Problema: Não consigo adicionar um item

- Certifique-se de preencher todos os campos obrigatórios.
- Verifique se a foto está no formato suportado.

##### Problema: O aplicativo está lento ou travando

- Tente reiniciar o aplicativo.
- Certifique-se de que sua conexão com a internet está estável.
- Atualize o aplicativo para a versão mais recente.

### Conclusão

Com este guia, você tem todas as informações necessárias para aproveitar ao máximo The Collector. Caso precise de mais assistência, entre em contato com o suporte dentro do aplicativo.

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

Diagramas e Mockups:
<br><br>
<img src="https://img.shields.io/badge/Excalidraw-5E81AC?style=for-the-badge&logo=excalidraw&logoColor=white">
<img src="https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white">
<img src="https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white">

