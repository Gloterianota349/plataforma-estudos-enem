

# 🎓 ENEM+ — Plataforma de Estudos com Inteligência Artificial

O **ENEM+** é uma plataforma de estudos desenvolvida para auxiliar estudantes na preparação para o Exame Nacional do Ensino Médio (ENEM). A aplicação reúne ferramentas de aprendizagem, acompanhamento de desempenho e recursos de inteligência artificial em uma interface interativa e intuitiva.

O projeto busca centralizar diferentes estratégias de preparação para o ENEM, permitindo que os estudantes pratiquem questões, realizem simulados, desenvolvam redações e organizem seus estudos em um único ambiente.

## ✨ Funcionalidades

### 📊 Dashboard e acompanhamento

- Visualização de questões respondidas e percentual de acertos.
- Acompanhamento da sequência de dias de estudo.
- Definição de metas semanais de questões e redações.
- Questão do dia para incentivar a prática contínua.
- Indicadores de desempenho acadêmico.

### 📝 Questões e simulados

- Banco de questões de demonstração, organizado por ano, área, disciplina e assunto.
- Questões de múltipla escolha com cinco alternativas.
- Filtros para explorar questões por diferentes critérios.
- Correção automática e identificação de respostas certas e erradas.
- Explicações das respostas com auxílio de inteligência artificial.
- Simulados com diferentes modalidades e limite de tempo.
- Resultado com quantidade de acertos, aproveitamento e gabarito.

### ✍️ Prática de redação com IA

- Seleção de temas de redações anteriores do ENEM.
- Possibilidade de inserir temas personalizados.
- Campo para escrever e desenvolver uma redação.
- Análise textual com base nas cinco competências avaliadas pelo ENEM.
- Feedback sobre pontos fortes e aspectos que podem ser melhorados.
- Estimativa de nota de 0 a 1000 gerada pela IA.

### 🤖 Ferramentas de inteligência artificial

A plataforma integra a API do Google Gemini para oferecer recursos de aprendizagem personalizados:

- **Tutor IA:** responde a dúvidas e explica conteúdos de maneira didática.
- **Plano de estudos:** cria um planejamento personalizado de quatro semanas com base nos objetivos, disponibilidade e dificuldades do estudante.
- **Resumos inteligentes:** gera materiais de revisão sobre assuntos selecionados.
- **Mapas mentais:** organiza conceitos e conteúdos em estruturas hierárquicas.
- **Flashcards:** cria cartões de perguntas e respostas para auxiliar na memorização.

### 📚 Aulas e conteúdos

- Seleção de conteúdos de Biologia, Física e História.
- Reprodução de videoaulas incorporadas do YouTube.
- Geração de resumos com inteligência artificial a partir dos tópicos selecionados.

### 🧠 Flashcards e memorização

- Criação de baralhos personalizados.
- Adição e exclusão de cartões.
- Navegação entre cartões.
- Alternância entre pergunta e resposta.
- Geração automática de dez flashcards sobre um assunto com IA.

### 📅 Organização e produtividade

- Calendário com registro das atividades de estudo.
- Histórico de questões respondidas por dia.
- Relatórios de desempenho por área, disciplina e assunto.
- Timer Pomodoro com ciclos de foco de 25 minutos, pausa de 5 minutos e pausa longa de 15 minutos.

### 🏆 Perfil e conquistas

- Perfil personalizável com diferentes avatares.
- Sistema de conquistas baseado no desempenho.
- Indicadores de progresso e atividades realizadas.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| React | Construção da interface e dos componentes |
| JavaScript / JSX | Lógica e estrutura da aplicação |
| Recharts | Visualização de dados e gráficos |
| Lucide React | Ícones da interface |
| Tailwind CSS | Estilização e design responsivo |
| Google Gemini API | Recursos de inteligência artificial |
| YouTube Embed | Reprodução de videoaulas |

## 🧩 Arquitetura da aplicação

A implementação atual concentra a interface, os componentes e a lógica de funcionamento em um único arquivo React.

O gerenciamento de estado é realizado principalmente com os hooks do React, como `useState`, `useEffect`, `useMemo`, `useContext` e `useRef`.

O `AppContext` centraliza informações compartilhadas, incluindo:

- Questões e respostas dos estudantes.
- Página atualmente selecionada.
- Baralhos e cartões de estudo.
- Perfil e avatar.
- Histórico de simulados.
- Metas semanais.

## 📂 Estrutura atual do repositório

```text
plataforma-estudos-enem/
│
├── LICENSE
│
└── plataforma_de_estudos_enem_com_ia_avan_ada.tsx
```

**Arquivo principal:** `plataforma_de_estudos_enem_com_ia_avan_ada.tsx`

Esse arquivo contém a implementação dos componentes, das páginas, do gerenciamento de estado e das integrações utilizadas pela plataforma.

> **Observação:** o repositório disponibiliza atualmente o código-fonte principal, não um projeto React completo com configuração própria de dependências e scripts de execução.

## 🚀 Executando o projeto

Para executar a aplicação, é necessário integrá-la a um ambiente React configurado.

### 1. Crie um projeto React

Uma opção é utilizar Vite:

```bash
npm create vite@latest enem-plus -- --template react
cd enem-plus
npm install
```

### 2. Instale as dependências

```bash
npm install recharts lucide-react
```

A aplicação utiliza classes do Tailwind CSS. Portanto, configure o Tailwind CSS no projeto hospedeiro antes de executar a interface.

### 3. Adicione o código-fonte

Baixe o arquivo principal deste repositório e coloque-o na pasta `src` do projeto React.

Ajuste a extensão para `.jsx`, caso necessário, e importe o componente principal no arquivo de entrada da aplicação.

### 4. Execute a aplicação

```bash
npm run dev
```

O Vite disponibilizará o endereço local para acessar a plataforma.

## 🤖 Integração com Google Gemini

A aplicação utiliza a API do Google Gemini para gerar conteúdos educacionais e respostas personalizadas.

Entre os recursos que dependem dessa integração estão:

- Explicações de questões.
- Correção e feedback de redações.
- Planos de estudos personalizados.
- Resumos de conteúdos.
- Geração de flashcards.
- Mapas mentais.
- Respostas do Tutor IA.

**Configuração necessária:** o código atual possui a variável `apiKey` vazia. Para habilitar os recursos de IA, será necessário configurar uma chave válida do Google Gemini.

Documentação oficial: [Google AI for Developers](https://ai.google.dev/gemini-api/docs).

> 🔐 **Segurança:** não coloque uma chave privada da API diretamente no código-fonte disponibilizado publicamente. Para uma implementação de produção, recomenda-se realizar as chamadas à API por meio de um backend, mantendo a chave em uma variável de ambiente protegida no servidor.

## ⚠️ Limitações da versão atual

O projeto está em desenvolvimento e possui algumas limitações importantes:

- **Persistência:** os dados são mantidos em memória pelo React. Ao recarregar a página, questões respondidas, metas, flashcards criados e histórico de simulados são reiniciados.
- **Banco de questões:** o conjunto de questões está definido diretamente no código e funciona como uma base de demonstração.
- **Simulados:** as modalidades apresentam diferentes quantidades de questões, mas a quantidade efetivamente disponível depende do tamanho do banco de questões carregado.
- **Inteligência artificial:** os recursos dependem da configuração e disponibilidade da API Gemini.
- **Perfil:** algumas métricas e lógicas de conquistas ainda precisam ser aperfeiçoadas.
- **Infraestrutura:** o repositório ainda não possui backend, banco de dados ou autenticação configurados.

## 💡 Possíveis evoluções

Algumas melhorias que podem ampliar as funcionalidades e a maturidade técnica da plataforma:

- Implementação de backend e banco de dados para persistência das informações.
- Sistema de autenticação e perfis individuais.
- Expansão do banco de questões com provas oficiais do ENEM.
- Integração com a Teoria de Resposta ao Item (TRI) para estimativas de desempenho.
- Histórico detalhado e evolução dos resultados.
- Aprimoramento da correção de redações.
- Geração de mapas mentais visuais e interativos.
- Sistema de recomendações de estudo baseado nas dificuldades individuais.
- Melhorias de acessibilidade e experiência em dispositivos móveis.

## 📄 Licença

Este projeto está disponibilizado sob a licença **MIT**.

Consulte o arquivo [LICENSE](LICENSE) para conhecer os termos de utilização, modificação e distribuição.

## 👨‍💻 Autor

**Guilherme Andrade**

- GitHub: [@Gloterianota349](https://github.com/Gloterianota349)

---

<p align="center">
  📚 <strong>ENEM+</strong>
  <br />
  Tecnologia e inteligência artificial a serviço da educação
  <br /><br />
  Desenvolvido com dedicação para tornar a preparação para o ENEM mais organizada, interativa e acessível 🚀
</p>

