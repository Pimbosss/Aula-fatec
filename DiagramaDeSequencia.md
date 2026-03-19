```mermaid
sequenceDiagram

	participant U as usuário
	participant P as plataforma
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


