```mermaid
sequenceDiagram

	participant U as usuário
	participant P as plataforma
	participant PA as pagamento
	participant C as carrinho
	participant B as biblioteca



U->>P: Usuário pesquisa o jogo
P->>B: Plataforma encontra o jogo na biblioteca
B-->>P: Biblioteca retorna o jogo a plataforma
P-->>U: Plataforma retorna o jogo ao usuario
U->>C: Usuario adiciona o jogo ao carrinho
C->>B: Carrinho procura o jogo na biblioteca
B-->>C: Biblioteca confirma o jogo
C-->>U: Jogo é adicionado ao carrinho do usuario
U->>P: Usuario solicita o pagamento
P->>PA: Plataforma manda a solicitação
PA-->>P: Envia a confirmação para a plataforma
P-->>U: Plataforma envia a confirmação para o usuario
U->>PA: Usuario escolhe a forma de pagamento
PA-->>U: Confirmação do pagamento
B->>U: Biblioteca envia o jogo ao usuario para a instalação
