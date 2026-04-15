📚 EduGame - Plataforma de Gamificação Educacional
<div align="center">
https://img.icons8.com/color/96/000000/game-controller.png

Plataforma de gamificação e machine learning para apoio à educação

https://img.shields.io/badge/license-MIT-blue.svg
https://img.shields.io/badge/status-MVP-green.svg
https://img.shields.io/badge/PRs-welcome-brightgreen.svg

</div>
📋 Sobre o Projeto
O EduGame é uma plataforma educacional inovadora que utiliza gamificação e machine learning para engajar alunos no processo de ensino-aprendizagem. Desenvolvido como parte do Edital 007/2021 da FAPESB - Governo Inteligente II, o projeto visa transformar a experiência educacional através de tecnologia e dados.

🎯 Objetivos
Engajar alunos através de mecânicas de jogos (XP, níveis, conquistas)

Fornecer ferramentas analíticas para professores e gestores

Utilizar machine learning para identificar padrões de aprendizado

Gerar relatórios inteligentes para tomada de decisão

Democratizar o acesso à educação de qualidade

🌟 Diferenciais
Sistema de Gamificação Completo: XP, níveis, badges, rankings

Machine Learning Aplicado: Recomendações personalizadas e insights

Multi-perfil: Aluno, Professor e Gestor com visões específicas

Relatórios Inteligentes: Dados para tomada de decisão educacional

Responsivo: Funciona em qualquer dispositivo

🚀 Demonstração
Login e Dashboard
https://via.placeholder.com/800x400?text=Login+Screen
https://via.placeholder.com/800x400?text=Dashboard+Aluno

Sistema de Quiz Gamificado
https://via.placeholder.com/800x400?text=Quiz+System

Painel do Professor
https://via.placeholder.com/800x400?text=Teacher+Panel

Relatórios e Analytics
https://via.placeholder.com/800x400?text=Reports

🛠️ Tecnologias Utilizadas
Frontend
HTML5 - Estrutura da aplicação

CSS3 - Estilização e responsividade

JavaScript (ES6+) - Lógica e interatividade

Font Awesome - Ícones e elementos visuais

Backend (Simulado)
API Fake - Simulação de backend para MVP

LocalStorage - Persistência de dados durante a sessão

Arquitetura
SPA-like - Navegação entre páginas sem recarregamento

Componentização - Código organizado por funcionalidades

Event-Driven - Comunicação baseada em eventos

📦 Instalação e Execução
Pré-requisitos
Navegador web moderno (Chrome, Firefox, Edge, Safari)

Conexão com internet (para carregar Font Awesome)

Instalação Local
Clone o repositório

bash
git clone https://github.com/seu-usuario/edugame.git
cd edugame
Abra o arquivo HTML

bash
# No Windows
start index.html

# No macOS
open index.html

# No Linux
xdg-open index.html
Ou use um servidor local

bash
# Usando Python
python -m http.server 8000

# Usando Node.js (http-server)
npx http-server

# Usando Live Server (VS Code)
# Instale a extensão Live Server e clique em "Go Live"
👥 Usuários de Teste
Perfil	Usuário	Senha	Funcionalidades
🎓 Aluno	joao	123456	Jogar quizzes, ver progresso, rankings
🎓 Aluna	maria	123456	Jogar quizzes, ver progresso, rankings
👨‍🏫 Professor	prof_carlos	123456	Gerenciar turmas, criar quizzes, ver analytics
👔 Gestor	gestor_ana	123456	Relatórios consolidados, visão estratégica
🎮 Funcionalidades
Para Alunos
✅ Dashboard personalizado com XP e nível

✅ Sistema de quizzes gamificados

✅ Conquistas e badges

✅ Ranking da turma

✅ Progresso por matéria

✅ Avatar evolutivo

Para Professores
✅ Visão geral das turmas

✅ Gerenciamento de quizzes

✅ Análise de desempenho por aluno

✅ Recomendações baseadas em ML

✅ Alertas de dificuldade por tópico

Para Gestores
✅ Relatórios consolidados

✅ Métricas de engajamento

✅ Insights estratégicos

✅ Exportação de dados

✅ Visão macro do ecossistema

📊 Estrutura do Projeto
text
edugame/
│
├── index.html              # Arquivo principal
├── README.md              # Documentação
├── LICENSE                # Licença MIT
│
├── css/
│   └── styles.css         # Estilos da aplicação
│
├── js/
│   ├── api.js            # API simulada
│   ├── app.js            # Lógica principal
│   ├── components.js     # Componentes reutilizáveis
│   └── utils.js          # Funções utilitárias
│
└── assets/
    ├── icons/            # Ícones da aplicação
    └── images/           # Imagens e logos
🔄 Fluxo da Aplicação
















🧠 Lógica de Gamificação
Sistema de XP (Experience Points)
Cada resposta correta: +50 XP (ajustável por quiz)

Uso de dica: -10 XP

Bônus por sequência: +25 XP

Conclusão de quiz: +100 XP

Níveis
Nível	XP Necessário	Título
1	0 - 999	Iniciante
2	1000 - 1999	Aprendiz
3	2000 - 2999	Explorador
4	3000 - 3999	Mestre
5	4000+	Lenda
Conquistas
Iniciante: Completar primeiro quiz

Curioso: Completar 5 quizzes

Rápido: Acertar 3 questões seguidas

Mestre: Atingir nível 4

Estrela: Acumular 2000 XP

Gênio: Completar todos os quizzes

🔮 Roadmap
Fase 1 - MVP (Atual) ✅
Sistema de login multi-perfil

Dashboard básico

Quizzes gamificados

Progresso do aluno

Relatórios simples

Fase 2 - Expansão (Em desenvolvimento)
Backend real (Node.js + PostgreSQL)

Autenticação JWT

Criação de quizzes pelo professor

Sistema de turmas completo

Chat e fóruns de discussão

Fase 3 - Machine Learning (Planejado)
Algoritmos de recomendação personalizada

Predição de dificuldade por aluno

Análise de padrões de aprendizado

Sistema de alerta preventivo

Dashboard avançado de analytics

Fase 4 - Mobile (Futuro)
Aplicativo React Native

Notificações push

Offline mode

Reconhecimento de voz

AR/VR para quizzes

🤝 Contribuição
Contribuições são super bem-vindas!

Como contribuir
Fork o projeto

Crie sua branch (git checkout -b feature/AmazingFeature)

Commit suas mudanças (git commit -m 'Add some AmazingFeature')

Push para a branch (git push origin feature/AmazingFeature)

Abra um Pull Request

Diretrizes
Mantenha o código limpo e documentado

Siga as convenções de nomenclatura

Teste antes de enviar

Atualize a documentação

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

🙏 Agradecimentos
FAPESB - Fundação de Amparo à Pesquisa do Estado da Bahia

Governo Inteligente II - Edital 007/2021

Vanmo - Empresa proponente do projeto

Hub Sudoeste - Espaço de inovação em Vitória da Conquista

UFRJ e IFBA - Parceiros acadêmicos

📞 Contato
Coordenador do Projeto

Nome: Ualdir Oliveira Santos Neto

Email: ualdir@yahoo.com

Vanmo

Email: contato@vanmo.com

Local: Vitória da Conquista - BA

📊 Métricas do Projeto
Métrica	Valor
Público-alvo	22.5M alunos (EF2 + EM)
Meta em 2 anos	1% do mercado útil (220k alunos)
Investimento	R$ 399.924,28
Prazo	16 meses
Equipe	4 funcionários + parceiros
🎯 Impacto Esperado
Melhoria no aprendizado: +30% em taxas de acerto

Engajamento: +50% na participação dos alunos

Tomada de decisão: Relatórios em tempo real

Inovação pedagógica: Nova metodologia disponível

Inclusão digital: Ferramenta offline-first

<div align="center">
Desenvolvido com ❤️ para a educação brasileira

⬆ Voltar ao topo

</div>
📝 Notas de Versão
v1.0.0 (MVP - Dezembro 2024)
Primeira versão estável

Sistema de login funcional

Quizzes completos

Dashboard dinâmico

Painel multi-perfil

Próximas versões
v1.1.0 - Backend real (Janeiro 2025)

v1.2.0 - Mobile app (Março 2025)

v2.0.0 - Machine learning completo (Junho 2025)

🐛 Reportar Bugs
Encontrou um bug? Por favor, abra uma issue com:

Descrição detalhada

Passos para reproduzir

Comportamento esperado vs atual

Screenshots (se aplicável)

Ambiente (navegador, SO)

⭐ Mostre seu apoio
Se este projeto te ajudou ou você gostou, dê uma ⭐ no GitHub! Isso nos motiva a continuar desenvolvendo.


