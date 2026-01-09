 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/scripts/app.js b/scripts/app.js
index ae47f8900a3f12db69ed8741985c7b194d316392..568f62842ed99cef88d50881ba0ceef24822c02a 100644
--- a/scripts/app.js
+++ b/scripts/app.js
@@ -1,1567 +1,1557 @@
- (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
-diff --git a/scripts/app.js b/scripts/app.js
-new file mode 100644
-index 0000000000000000000000000000000000000000..568f62842ed99cef88d50881ba0ceef24822c02a
---- /dev/null
-+++ b/scripts/app.js
-@@ -0,0 +1,1557 @@
-+/* ===========================================
-+   BACKEND SIMULADO (API FAKE)
-+   =========================================== */
-+const EduGameAPI = (() => {
-+    const db = {
-+        users: {
-+            'joao': {
-+                id: 1,
-+                username: 'joao',
-+                nome: 'João Silva',
-+                sigla: 'JS',
-+                role: 'aluno',
-+                cidade: 'Vitória da Conquista, BA',
-+                xp: 1850,
-+                nivel: 3,
-+                rankingTurma: 5,
-+                totalAlunos: 32,
-+                turma: '8º Ano A',
-+                escola: 'Escola Municipal São Paulo'
-+            },
-+            'maria': {
-+                id: 2,
-+                username: 'maria',
-+                nome: 'Maria Oliveira',
-+                sigla: 'MO',
-+                role: 'aluna',
-+                cidade: 'Vitória da Conquista, BA',
-+                xp: 2300,
-+                nivel: 4,
-+                rankingTurma: 2,
-+                totalAlunos: 32,
-+                turma: '8º Ano A',
-+                escola: 'Escola Municipal São Paulo'
-+            },
-+            'prof_carlos': {
-+                id: 3,
-+                username: 'prof_carlos',
-+                nome: 'Prof. Carlos Santos',
-+                sigla: 'CS',
-+                role: 'professor',
-+                cidade: 'Vitória da Conquista, BA',
-+                xp: 0,
-+                nivel: 0,
-+                turmas: ['8º Ano A', '9º Ano B', '7º Ano C'],
-+                escola: 'Escola Municipal São Paulo'
-+            },
-+            'gestor_ana': {
-+                id: 4,
-+                username: 'gestor_ana',
-+                nome: 'Ana Souza',
-+                sigla: 'AS',
-+                role: 'gestor',
-+                cidade: 'Vitória da Conquista, BA',
-+                xp: 0,
-+                nivel: 0,
-+                escola: 'Secretaria Municipal de Educação'
-+            }
-+        },
-+
-+        quizzes: [
-+            {
-+                id: 1,
-+                materia: 'Matemática',
-+                unidade: 'Unidade 3: Geometria',
-+                descricao: 'Conceitos básicos de geometria plana',
-+                dificuldade: 'Fácil',
-+                ganhoXpPorQuestao: 50,
-+                perdaXpDica: 10,
-+                totalQuestoes: 3,
-+                completado: false,
-+                questoes: [
-+                    {
-+                        id: 1,
-+                        enunciado: 'Qual é a fórmula para calcular a área de um triângulo?',
-+                        alternativas: [
-+                            'A = b × h',
-+                            'A = (b × h) / 2',
-+                            'A = π × r²',
-+                            'A = l²'
-+                        ],
-+                        correta: 1,
-+                        dica: 'A fórmula envolve base e altura, mas não é simplesmente a multiplicação das duas.'
-+                    },
-+                    {
-+                        id: 2,
-+                        enunciado: 'Um triângulo tem base de 10 cm e altura de 6 cm. Qual é sua área?',
-+                        alternativas: [
-+                            '60 cm²',
-+                            '30 cm²',
-+                            '15 cm²',
-+                            '20 cm²'
-+                        ],
-+                        correta: 1,
-+                        dica: 'Use a fórmula da área do triângulo: (base × altura) / 2'
-+                    },
-+                    {
-+                        id: 3,
-+                        enunciado: 'Qual é a soma dos ângulos internos de um triângulo?',
-+                        alternativas: [
-+                            '90º',
-+                            '180º',
-+                            '270º',
-+                            '360º'
-+                        ],
-+                        correta: 1,
-+                        dica: 'Pense na soma dos ângulos internos de qualquer triângulo.'
-+                    }
-+                ]
-+            },
-+            {
-+                id: 2,
-+                materia: 'Português',
-+                unidade: 'Unidade 2: Análise Sintática',
-+                descricao: 'Identificação de sujeito e predicado',
-+                dificuldade: 'Médio',
-+                ganhoXpPorQuestao: 75,
-+                perdaXpDica: 15,
-+                totalQuestoes: 3,
-+                completado: true,
-+                questoes: [
-+                    {
-+                        id: 1,
-+                        enunciado: 'Na frase "O aluno estudou para a prova", qual é o sujeito?',
-+                        alternativas: [
-+                            'O aluno',
-+                            'estudou',
-+                            'para a prova',
-+                            'prova'
-+                        ],
-+                        correta: 0,
-+                        dica: 'O sujeito é quem pratica a ação do verbo.'
-+                    }
-+                ]
-+            },
-+            {
-+                id: 3,
-+                materia: 'Ciências',
-+                unidade: 'Unidade 1: Sistema Solar',
-+                descricao: 'Planetas e características do sistema solar',
-+                dificuldade: 'Fácil',
-+                ganhoXpPorQuestao: 50,
-+                perdaXpDica: 10,
-+                totalQuestoes: 4,
-+                completado: false,
-+                questoes: [
-+                    {
-+                        id: 1,
-+                        enunciado: 'Qual é o maior planeta do sistema solar?',
-+                        alternativas: [
-+                            'Terra',
-+                            'Júpiter',
-+                            'Saturno',
-+                            'Netuno'
-+                        ],
-+                        correta: 1,
-+                        dica: 'É conhecido por sua grande mancha vermelha.'
-+                    }
-+                ]
-+            }
-+        ],
-+
-+        progresso: {
-+            'joao': {
-+                atividadesSemana: 12,
-+                materias: [
-+                    { nome: 'Matemática', percentual: 85, xp: 850 },
-+                    { nome: 'Português', percentual: 72, xp: 600 },
-+                    { nome: 'Ciências', percentual: 64, xp: 400 }
-+                ],
-+                avatar: {
-+                    nivel: 3,
-+                    titulo: 'Explorador do Conhecimento',
-+                    itens: [
-+                        'Capacete de bronze (completou 10 quizzes)',
-+                        'Espada do saber (atingiu 1000 XP)',
-+                        'Escudo da persistência (5 dias consecutivos de atividade)'
-+                    ]
-+                },
-+                badges: [
-+                    { id: 1, nome: 'Iniciante', icone: 'fas fa-rocket', desbloqueado: true },
-+                    { id: 2, nome: 'Curioso', icone: 'fas fa-brain', desbloqueado: true },
-+                    { id: 3, nome: 'Rápido', icone: 'fas fa-bolt', desbloqueado: true },
-+                    { id: 4, nome: 'Mestre', icone: 'fas fa-crown', desbloqueado: false },
-+                    { id: 5, nome: 'Estrela', icone: 'fas fa-star', desbloqueado: true },
-+                    { id: 6, nome: 'Gênio', icone: 'fas fa-gem', desbloqueado: false }
-+                ]
-+            },
-+            'maria': {
-+                atividadesSemana: 18,
-+                materias: [
-+                    { nome: 'Matemática', percentual: 92, xp: 1200 },
-+                    { nome: 'Português', percentual: 88, xp: 800 },
-+                    { nome: 'Ciências', percentual: 78, xp: 300 }
-+                ],
-+                avatar: {
-+                    nivel: 4,
-+                    titulo: 'Mestre do Conhecimento',
-+                    itens: [
-+                        'Capacete de prata (completou 20 quizzes)',
-+                        'Espada lendária (atingiu 2000 XP)',
-+                        'Escudo da sabedoria (10 dias consecutivos de atividade)'
-+                    ]
-+                },
-+                badges: [
-+                    { id: 1, nome: 'Iniciante', icone: 'fas fa-rocket', desbloqueado: true },
-+                    { id: 2, nome: 'Curioso', icone: 'fas fa-brain', desbloqueado: true },
-+                    { id: 3, nome: 'Rápido', icone: 'fas fa-bolt', desbloqueado: true },
-+                    { id: 4, nome: 'Mestre', icone: 'fas fa-crown', desbloqueado: true },
-+                    { id: 5, nome: 'Estrela', icone: 'fas fa-star', desbloqueado: true },
-+                    { id: 6, nome: 'Gênio', icone: 'fas fa-gem', desbloqueado: false }
-+                ]
-+            }
-+        },
-+
-+        reports: {
-+            desempenhoTurma: {
-+                mediaAcertos: 78,
-+                topicoMaisAcertado: 'Álgebra',
-+                topicoMenosAcertado: 'Geometria'
-+            },
-+            topicosDificuldade: [
-+                'Geometria',
-+                'Frações',
-+                'Análise Sintática'
-+            ],
-+            engajamento: {
-+                destaque: 'Maior atividade às terças e quintas-feiras.',
-+                picoHorario: '14h às 16h',
-+                taxaUso: '85% dos alunos usam a plataforma semanalmente'
-+            },
-+            rankingXp: {
-+                top5: [
-+                    { nome: 'Carlos Mendes', xp: 2800 },
-+                    { nome: 'Maria Oliveira', xp: 2300 },
-+                    { nome: 'Ana Costa', xp: 2100 },
-+                    { nome: 'Pedro Santos', xp: 1950 },
-+                    { nome: 'João Silva', xp: 1850 }
-+                ]
-+            }
-+        },
-+
-+        atividades: []
-+    };
-+
-+    function delay(data, ms = 400) {
-+        return new Promise(resolve => {
-+            setTimeout(() => resolve(JSON.parse(JSON.stringify(data))), ms);
-+        });
-+    }
-+
-+    return {
-+        login(username, password) {
-+            if (password !== '123456') {
-+                return delay({ success: false, message: 'Senha incorreta' });
-+            }
-+            const user = db.users[username];
-+            if (!user) {
-+                return delay({ success: false, message: 'Usuário não encontrado' });
-+            }
-+            db.atividades.push({ usuario: username, tipo: 'login', timestamp: new Date().toISOString() });
-+            return delay({
-+                success: true,
-+                user: { ...user },
-+                token: 'fake-jwt-' + Date.now()
-+            });
-+        },
-+
-+        logout(username) {
-+            if (username) {
-+                db.atividades.push({ usuario: username, tipo: 'logout', timestamp: new Date().toISOString() });
-+            }
-+            return delay({ success: true });
-+        },
-+
-+        getUser(username) {
-+            const user = db.users[username];
-+            if (!user) return delay(null);
-+            return delay({ ...user });
-+        },
-+
-+        getDashboard(username) {
-+            const user = db.users[username];
-+            if (!user) return delay(null);
-+            const progresso = db.progresso[username] || db.progresso['joao'];
-+            return delay({
-+                totalXp: user.xp,
-+                nivelAtual: user.nivel,
-+                xpProximoNivel: (user.nivel + 1) * 1000 - user.xp,
-+                conquistasDesbloqueadas: progresso.badges.filter(b => b.desbloqueado).length,
-+                conquistasTotal: progresso.badges.length,
-+                quizCompletos: db.quizzes.filter(q => q.completado).length,
-+                quizRestantes: db.quizzes.filter(q => !q.completado).length,
-+                rankingPosicao: user.rankingTurma || 5,
-+                rankingTotal: user.totalAlunos || 32,
-+                distanciaProximoColocadoXp: 150
-+            });
-+        },
-+
-+        getQuizzes() {
-+            return delay(db.quizzes);
-+        },
-+
-+        getQuizById(id) {
-+            const quiz = db.quizzes.find(q => q.id === id);
-+            return delay(quiz ? { ...quiz } : null);
-+        },
-+
-+        submitAnswer({ username, quizId, questionId, alternativaIndex }) {
-+            const user = db.users[username];
-+            const quiz = db.quizzes.find(q => q.id === quizId);
-+            if (!user || !quiz) {
-+                return delay({ correto: false, xpGanho: 0, xpTotal: user?.xp || 0 });
-+            }
-+            const questao = quiz.questoes.find(q => q.id === questionId);
-+            if (!questao) {
-+                return delay({ correto: false, xpGanho: 0, xpTotal: user.xp });
-+            }
-+            const correto = (questao.correta === alternativaIndex);
-+            const xpGanho = correto ? quiz.ganhoXpPorQuestao : 0;
-+            user.xp += xpGanho;
-+
-+            db.atividades.push({
-+                usuario: username,
-+                tipo: 'quiz_resposta',
-+                quizId,
-+                questionId,
-+                correto,
-+                xpGanho,
-+                timestamp: new Date().toISOString()
-+            });
-+
-+            return delay({
-+                correto,
-+                xpGanho,
-+                xpTotal: user.xp,
-+                respostaCorreta: questao.correta
-+            });
-+        },
-+
-+        consumirDica(username, quizId) {
-+            const user = db.users[username];
-+            const quiz = db.quizzes.find(q => q.id === quizId);
-+            const custo = quiz ? quiz.perdaXpDica : 10;
-+            if (user) {
-+                user.xp = Math.max(0, user.xp - custo);
-+                db.atividades.push({
-+                    usuario: username,
-+                    tipo: 'quiz_dica',
-+                    quizId,
-+                    custo,
-+                    timestamp: new Date().toISOString()
-+                });
-+            }
-+            return delay({ xpTotal: user?.xp || 0, custo });
-+        },
-+
-+        getProgress(username) {
-+            const progresso = db.progresso[username] || db.progresso['joao'];
-+            return delay({ ...progresso });
-+        },
-+
-+        getReports(username) {
-+            const user = db.users[username];
-+            let reports = { ...db.reports };
-+
-+            if (user?.role === 'professor' || user?.role === 'gestor') {
-+                reports = {
-+                    ...reports,
-+                    insightsProfessor: [
-+                        '35% dos alunos melhoraram o desempenho após usar gamificação',
-+                        'Taxa de conclusão de quizzes aumentou 42%',
-+                        'Alunos engajados têm 28% menos faltas'
-+                    ],
-+                    recomendacoesML: [
-+                        'Revisar tópico de Geometria com turma 8º Ano A',
-+                        'Incentivar uso da plataforma às segundas-feiras (menor engajamento)',
-+                        'Criar quiz sobre Frações para reforço'
-+                    ]
-+                };
-+            }
-+            return delay(reports);
-+        },
-+
-+        completeQuiz(username, quizId) {
-+            const quiz = db.quizzes.find(q => q.id === quizId);
-+            if (!quiz) return delay({ success: false });
-+            quiz.completado = true;
-+            db.atividades.push({
-+                usuario: username,
-+                tipo: 'quiz_completado',
-+                quizId,
-+                materia: quiz.materia,
-+                timestamp: new Date().toISOString()
-+            });
-+            return delay({ success: true, quiz });
-+        },
-+
-+        getRecentActivities(username, limit = 5) {
-+            const atividades = db.atividades
-+                .filter(a => a.usuario === username)
-+                .sort((a, b) => new Date(b.timestamp) - new Date(a.timestamp))
-+                .slice(0, limit);
-+            return delay(atividades);
-+        },
-+
-+        // Nova função "tipo ML": recomenda próximo foco para o aluno
-+        getRecommendation(username) {
-+            const progresso = db.progresso[username] || db.progresso['joao'];
-+            const materiasOrdenadas = [...progresso.materias].sort((a, b) => a.percentual - b.percentual);
-+            const materiaMaisFraca = materiasOrdenadas[0];
-+
-+            let mensagem = 'Você está indo muito bem!';
-+            let acao = 'Continue praticando nos quizzes disponíveis.';
-+
-+            if (materiaMaisFraca) {
-+                mensagem = `Seu ponto de atenção é ${materiaMaisFraca.nome}.`;
-+                acao = `Recomendamos focar em quizzes de ${materiaMaisFraca.nome} para melhorar seu desempenho.`;
-+            }
-+
-+            return delay({
-+                materiaFoco: materiaMaisFraca?.nome || null,
-+                mensagem,
-+                acao
-+            });
-+        }
-+    };
-+})();
-+
-+/* ===========================================
-+   PAPÉIS DE USUÁRIO
-+   =========================================== */
-+const ROLES = {
-+    ALUNO: 'aluno',
-+    ALUNA: 'aluna',
-+    PROFESSOR: 'professor',
-+    GESTOR: 'gestor'
-+};
-+
-+/* ===========================================
-+   GERENCIAMENTO DE ESTADO
-+   =========================================== */
-+const AppState = {
-+    currentUser: null,
-+    userData: null,
-+    dashboard: null,
-+    quizzes: [],
-+    currentQuiz: null,
-+    currentQuestionIndex: 0,
-+    userAnswers: {},
-+
-+    async init(username) {
-+        try {
-+            const userData = await EduGameAPI.getUser(username);
-+            this.currentUser = username;
-+            this.userData = userData;
-+
-+            const [dashboard, quizzes] = await Promise.all([
-+                EduGameAPI.getDashboard(username),
-+                EduGameAPI.getQuizzes()
-+            ]);
-+
-+            this.dashboard = dashboard;
-+            this.quizzes = quizzes;
-+            this.currentQuiz = quizzes.find(q => !q.completado) || quizzes[0] || null;
-+            return true;
-+        } catch (e) {
-+            console.error('Erro ao inicializar AppState:', e);
-+            return false;
-+        }
-+    },
-+
-+    reset() {
-+        this.currentUser = null;
-+        this.userData = null;
-+        this.dashboard = null;
-+        this.quizzes = [];
-+        this.currentQuiz = null;
-+        this.currentQuestionIndex = 0;
-+        this.userAnswers = {};
-+    },
-+
-+    async refreshDashboard() {
-+        if (!this.currentUser) return;
-+        this.dashboard = await EduGameAPI.getDashboard(this.currentUser);
-+        this.userData = await EduGameAPI.getUser(this.currentUser);
-+    }
-+};
-+
-+/* ===========================================
-+   UI / UTILITÁRIOS VISUAIS
-+   =========================================== */
-+const UI = {
-+    showNotification(message, type = 'success', duration = 3000) {
-+        const existing = document.querySelector('.notification');
-+        if (existing) existing.remove();
-+
-+        const notification = document.createElement('div');
-+        notification.className = `notification ${type}`;
-+        notification.setAttribute('role', 'alert');
-+        notification.setAttribute('aria-live', 'assertive');
-+        notification.innerHTML = `
-+            <div style="display: flex; align-items: flex-start; gap: 10px;">
-+                <div style="font-size: 1.2rem;">
-+                    ${type === 'success' ? '✓' : type === 'error' ? '✗' : '!'}
-+                </div>
-+                <div>${message}</div>
-+            </div>
-+        `;
-+        document.body.appendChild(notification);
-+
-+        setTimeout(() => {
-+            if (notification.parentNode) {
-+                notification.parentNode.removeChild(notification);
-+            }
-+        }, duration);
-+    },
-+
-+    showLoading(show) {
-+        const loadingEl = document.getElementById('loading');
-+        if (!loadingEl) return;
-+        if (show) {
-+            loadingEl.classList.add('active');
-+        } else {
-+            loadingEl.classList.remove('active');
-+        }
-+    },
-+
-+    // Alterna apenas entre tela de login e app
-+    showScreen(screenId) {
-+        const login = document.getElementById('login-screen');
-+        const app = document.getElementById('app');
-+
-+        if (login) {
-+            login.style.display = (screenId === 'login-screen') ? 'block' : 'none';
-+        }
-+        if (app) {
-+            app.style.display = (screenId === 'app') ? 'block' : 'none';
-+        }
-+    },
-+
-+    // Menu diferente por papel
-+    updateNavigation(role) {
-+        const teacherNav = document.getElementById('teacher-nav');
-+        const navItems = {
-+            dashboard: document.querySelector('a.nav-link[data-page="dashboard"]')?.parentElement,
-+            quizzes: document.querySelector('a.nav-link[data-page="quizzes"]')?.parentElement,
-+            quizPlay: document.querySelector('a.nav-link[data-page="quiz-play"]')?.parentElement,
-+            progress: document.querySelector('a.nav-link[data-page="progress"]')?.parentElement,
-+            reports: document.querySelector('a.nav-link[data-page="reports"]')?.parentElement,
-+            teacher: teacherNav
-+        };
-+
-+        Object.values(navItems).forEach(li => {
-+            if (li) li.style.display = '';
-+        });
-+
-+        if (role === ROLES.ALUNO || role === ROLES.ALUNA) {
-+            if (navItems.teacher) navItems.teacher.style.display = 'none';
-+        } else if (role === ROLES.PROFESSOR) {
-+            if (navItems.teacher) navItems.teacher.style.display = '';
-+        } else if (role === ROLES.GESTOR) {
-+            if (navItems.quizzes) navItems.quizzes.style.display = 'none';
-+            if (navItems.quizPlay) navItems.quizPlay.style.display = 'none';
-+            if (navItems.progress) navItems.progress.style.display = 'none';
-+            if (navItems.teacher) navItems.teacher.style.display = '';
-+        }
-+    }
-+};
-+
-+/* ===========================================
-+   RENDERIZAÇÃO
-+   =========================================== */
-+const Render = {
-+    renderHeader(user) {
-+        const avatar = document.getElementById('user-avatar');
-+        const name = document.getElementById('user-name');
-+        if (avatar) avatar.textContent = user.sigla || user.nome.substring(0, 2).toUpperCase();
-+        if (name) name.textContent = user.nome;
-+
-+        const subtitle = document.getElementById('dashboard-subtitle');
-+        if (subtitle) {
-+            if (user.role === ROLES.PROFESSOR) {
-+                subtitle.textContent = `Olá, ${user.nome}. Acompanhe o desempenho das suas turmas.`;
-+            } else if (user.role === ROLES.GESTOR) {
-+                subtitle.textContent = `Olá, ${user.nome}. Veja os indicadores para tomada de decisão.`;
-+            } else {
-+                subtitle.textContent = `Olá, ${user.nome}. Vamos avançar no seu aprendizado?`;
-+            }
-+        }
-+    },
-+
-+        async renderDashboard(dashboard, user) {
-+        const role = user.role;
-+        const cardsContainer = document.querySelector('.dashboard-cards');
-+
-+        // ============================
-+        // DASHBOARD DE PROFESSOR
-+        // ============================
-+        if (role === ROLES.PROFESSOR && cardsContainer) {
-+            // Esconde elementos típicos de aluno
-+            const recCard = document.getElementById('recomendacao-card');
-+            if (recCard) recCard.style.display = 'none';
-+            const badgesContainer = document.getElementById('badges-container');
-+            if (badgesContainer) badgesContainer.style.display = 'none';
-+
-+            const turmasAtivas = Array.isArray(user.turmas) ? user.turmas.length : 0;
-+
-+            cardsContainer.innerHTML = `
-+                <div class="card">
-+                    <h3><i class="fas fa-users"></i> Minhas turmas</h3>
-+                    <div class="stat">${turmasAtivas}</div>
-+                    <p>Turmas acompanhadas na plataforma</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 75%"></div>
-+                    </div>
-+                    <p>Meta: ampliar o uso da plataforma em todas as turmas.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-question-circle"></i> Quizzes ativos</h3>
-+                    <div class="stat">15</div>
-+                    <p>Quizzes disponíveis para os alunos</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 60%"></div>
-+                    </div>
-+                    <p>Use o painel do professor para criar e ajustar quizzes.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-chart-line"></i> Desempenho médio</h3>
-+                    <div class="stat">78%</div>
-+                    <p>Média de acertos das turmas</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 78%"></div>
-+                    </div>
-+                    <p>Meta: chegar a 85% de acertos.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-bell"></i> Pontos de atenção</h3>
-+                    <p><strong>Conteúdos com maior dificuldade:</strong></p>
-+                    <ul style="margin-top:10px; padding-left:18px;">
-+                        <li>Geometria (8º Ano A)</li>
-+                        <li>Frações (7º Ano C)</li>
-+                    </ul>
-+                    <p style="margin-top:10px;">Planeje revisões focadas usando os relatórios analíticos.</p>
-+                </div>
-+            `;
-+
-+            // Já ajustamos tudo para professor, não precisamos da lógica de aluno
-+            return;
-+        }
-+
-+        // ============================
-+        // DASHBOARD DE GESTOR
-+        // ============================
-+        if (role === ROLES.GESTOR && cardsContainer) {
-+            const recCard = document.getElementById('recomendacao-card');
-+            if (recCard) recCard.style.display = 'none';
-+            const badgesContainer = document.getElementById('badges-container');
-+            if (badgesContainer) badgesContainer.style.display = 'none';
-+
-+            cardsContainer.innerHTML = `
-+                <div class="card">
-+                    <h3><i class="fas fa-school"></i> Escolas conectadas</h3>
-+                    <div class="stat">12</div>
-+                    <p>Unidades utilizando a plataforma</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 70%"></div>
-+                    </div>
-+                    <p>Meta: expandir o uso para toda a rede.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-users"></i> Engajamento dos alunos</h3>
-+                    <div class="stat">85%</div>
-+                    <p>Alunos que acessam a plataforma semanalmente</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 85%"></div>
-+                    </div>
-+                    <p>Priorizar escolas com engajamento abaixo de 60%.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-chart-line"></i> Desempenho da rede</h3>
-+                    <div class="stat">78%</div>
-+                    <p>Média geral de acertos em quizzes</p>
-+                    <div class="progress-bar">
-+                        <div class="progress-fill" style="width: 78%"></div>
-+                    </div>
-+                    <p>Foco em áreas críticas como Geometria e Frações.</p>
-+                </div>
-+
-+                <div class="card">
-+                    <h3><i class="fas fa-bullseye"></i> Prioridades estratégicas</h3>
-+                    <ul style="margin-top:10px; padding-left:18px;">
-+                        <li>Aumentar o uso da plataforma nas turmas finais do Fundamental.</li>
-+                        <li>Monitorar risco de evasão via engajamento na plataforma.</li>
-+                        <li>Planejar formações de professores com base nos dados.</li>
-+                    </ul>
-+                </div>
-+            `;
-+
-+            return;
-+        }
-+
-+        // ============================
-+        // DASHBOARD DE ALUNO / ALUNA
-+        // ============================
-+        // Garante que os elementos "gamificados" estejam visíveis
-+        const badgesContainer = document.getElementById('badges-container');
-+        if (badgesContainer) badgesContainer.style.display = 'flex';
-+        const recCard = document.getElementById('recomendacao-card');
-+        if (recCard) recCard.style.display = '';
-+
-+        // XP Total
-+        const xpElement = document.getElementById('total-xp');
-+        if (xpElement) xpElement.textContent = `${dashboard.totalXp.toLocaleString('pt-BR')} XP`;
-+
-+        // Nível
-+        const nivelElement = document.getElementById('nivel-text');
-+        if (nivelElement) nivelElement.textContent = `Você está no nível ${dashboard.nivelAtual}`;
-+
-+        // Progresso para próximo nível
-+        const totalParaProximo = dashboard.totalXp + dashboard.xpProximoNivel;
-+        const xpPercent = Math.min(100, (dashboard.totalXp / totalParaProximo) * 100);
-+
-+        const xpProgress = document.getElementById('xp-progress');
-+        if (xpProgress) xpProgress.style.width = `${xpPercent}%`;
-+
-+        const proximoElement = document.getElementById('proximo-nivel-text');
-+        if (proximoElement) proximoElement.textContent = `${dashboard.xpProximoNivel} XP para o próximo nível`;
-+
-+        const xpText = document.getElementById('xp-text');
-+        if (xpText) xpText.textContent = `${dashboard.totalXp.toLocaleString('pt-BR')} / ${totalParaProximo.toLocaleString('pt-BR')}`;
-+
-+        const xpBarFill = document.getElementById('xp-bar-fill');
-+        if (xpBarFill) xpBarFill.style.width = `${xpPercent}%`;
-+
-+        // Conquistas
-+        const conquistasStat = document.getElementById('conquistas-stat');
-+        if (conquistasStat) conquistasStat.textContent = `${dashboard.conquistasDesbloqueadas}/${dashboard.conquistasTotal}`;
-+
-+        const conquistasProgress = document.getElementById('conquistas-progress');
-+        if (conquistasProgress) {
-+            const percentConq = Math.round((dashboard.conquistasDesbloqueadas / dashboard.conquistasTotal) * 100);
-+            conquistasProgress.style.width = `${percentConq}%`;
-+        }
-+
-+        // Quizzes
-+        const quizCompletos = document.getElementById('quiz-completos');
-+        if (quizCompletos) quizCompletos.textContent = dashboard.quizCompletos;
-+
-+        const quizRestantes = document.getElementById('quiz-restantes');
-+        if (quizRestantes) quizRestantes.textContent = `${dashboard.quizRestantes} quiz restantes nesta unidade`;
-+
-+        // Ranking
-+        const rankingPosicao = document.getElementById('ranking-posicao');
-+        if (rankingPosicao) rankingPosicao.textContent = `#${dashboard.rankingPosicao}`;
-+
-+        const rankingTotal = document.getElementById('ranking-total');
-+        if (rankingTotal) rankingTotal.textContent = `Entre ${dashboard.rankingTotal} alunos`;
-+
-+        const distanciaProximo = document.getElementById('distancia-proximo');
-+        if (distanciaProximo) distanciaProximo.textContent = `${dashboard.distanciaProximoColocadoXp} XP atrás do ${dashboard.rankingPosicao}º lugar`;
-+
-+        // Gamificação: badges + recomendação "tipo ML"
-+        await this.renderBadges(user);
-+        await this.renderRecommendation(user);
-+    }
-+,
-+
-+    async renderBadges(user) {
-+        const badgesContainer = document.getElementById('badges-container');
-+        if (!badgesContainer) return;
-+
-+        const progress = await EduGameAPI.getProgress(user.username);
-+        badgesContainer.innerHTML = '';
-+
-+        progress.badges.forEach(badge => {
-+            const badgeElement = document.createElement('div');
-+            badgeElement.className = `badge ${badge.desbloqueado ? '' : 'locked'}`;
-+            badgeElement.innerHTML = `<i class="${badge.icone}"></i>`;
-+            badgeElement.title = `${badge.nome} - ${badge.desbloqueado ? 'Desbloqueado' : 'Bloqueado'}`;
-+            badgesContainer.appendChild(badgeElement);
-+        });
-+    },
-+
-+    // Card de recomendação “tipo ML”
-+    async renderRecommendation(user) {
-+        if (!(user.role === ROLES.ALUNO || user.role === ROLES.ALUNA)) {
-+            const card = document.getElementById('recomendacao-card');
-+            if (card) card.style.display = 'none';
-+            return;
-+        }
-+        const rec = await EduGameAPI.getRecommendation(user.username);
-+        const card = document.getElementById('recomendacao-card');
-+        const msg = document.getElementById('recomendacao-mensagem');
-+        const acao = document.getElementById('recomendacao-acao');
-+        if (card && msg && acao && rec) {
-+            msg.textContent = rec.mensagem;
-+            acao.textContent = rec.acao;
-+            card.style.display = 'block';
-+        }
-+    },
-+
-+    renderQuizzesList(quizzes, userRole) {
-+        const quizzesList = document.getElementById('quizzes-list');
-+        const playQuizList = document.getElementById('play-quiz-list');
-+
-+        const renderToElement = (element) => {
-+            if (!element) return;
-+            element.innerHTML = '';
-+
-+            if (!quizzes || quizzes.length === 0) {
-+                element.innerHTML = `
-+                    <div class="card">
-+                        <h3><i class="fas fa-info-circle"></i> Nenhum quiz disponível</h3>
-+                        <p>Peça ao seu professor para liberar novos quizzes ou revise os conteúdos já estudados.</p>
-+                    </div>
-+                `;
-+                return;
-+            }
-+
-+            quizzes.forEach(quiz => {
-+                const quizCard = document.createElement('div');
-+                quizCard.className = 'quiz-card';
-+
-+                const dificuldadeColor = {
-+                    'Fácil': '#4CAF50',
-+                    'Médio': '#FF9800',
-+                    'Difícil': '#F44336'
-+                }[quiz.dificuldade] || '#757575';
-+
-+                quizCard.innerHTML = `
-+                    <h4>${quiz.materia}</h4>
-+                    <p><strong>${quiz.unidade}</strong></p>
-+                    <p style="margin: 10px 0;">${quiz.descricao}</p>
-+                    <div class="quiz-meta">
-+                        <div>
-+                            <span style="display: inline-block; width: 10px; height: 10px; background-color: ${dificuldadeColor}; border-radius: 50%; margin-right: 5px;"></span>
-+                            ${quiz.dificuldade}
-+                        </div>
-+                        <div>
-+                            <i class="fas fa-star" style="color: #FFC107;"></i>
-+                            ${quiz.ganhoXpPorQuestao} XP/questão
-+                        </div>
-+                    </div>
-+                `;
-+
-+                const actionsWrapper = document.createElement('div');
-+                actionsWrapper.style.marginTop = '15px';
-+
-+                const isAluno = (userRole === ROLES.ALUNO || userRole === ROLES.ALUNA);
-+                const isProfessor = (userRole === ROLES.PROFESSOR);
-+                const isGestor = (userRole === ROLES.GESTOR);
-+
-+                if ((isAluno || isProfessor) && quiz.completado) {
-+                    actionsWrapper.innerHTML = `
-+                        <div style="padding: 8px; background-color: #E8F5E9; border-radius: 4px; text-align: center; color: #2E7D32;">
-+                            <i class="fas fa-check-circle"></i> Concluído
-+                        </div>
-+                    `;
-+                } else {
-+                    if (isAluno) {
-+                        actionsWrapper.innerHTML = `
-+                            <button class="btn btn-primary btn-play-quiz" data-quiz-id="${quiz.id}" style="width: 100%;">
-+                                <i class="fas fa-play"></i> Jogar
-+                            </button>
-+                        `;
-+                    } else if (isProfessor) {
-+                        actionsWrapper.innerHTML = `
-+                            <div style="display: flex; gap: 10px;">
-+                                <button class="btn btn-primary btn-play-quiz" data-quiz-id="${quiz.id}" style="flex: 1;">
-+                                    <i class="fas fa-play"></i> Visualizar/Jogar
-+                                </button>
-+                                <button class="btn btn-secondary btn-edit-quiz" data-quiz-id="${quiz.id}" style="flex: 1;">
-+                                    <i class="fas fa-edit"></i> Editar
-+                                </button>
-+                            </div>
-+                        `;
-+                    } else if (isGestor) {
-+                        actionsWrapper.innerHTML = `
-+                            <button class="btn btn-secondary btn-view-quiz-reports" data-quiz-id="${quiz.id}" style="width: 100%;">
-+                                <i class="fas fa-chart-bar"></i> Ver desempenho deste quiz
-+                            </button>
-+                        `;
-+                    }
-+                }
-+
-+                quizCard.appendChild(actionsWrapper);
-+                element.appendChild(quizCard);
-+            });
-+        };
-+
-+        if (quizzesList) renderToElement(quizzesList);
-+        if (playQuizList) renderToElement(playQuizList);
-+    },
-+
-+    renderQuizGame(quiz, questionIndex) {
-+        const quizGame = document.getElementById('quiz-game');
-+        const quizSelection = document.getElementById('quiz-selection');
-+        if (!quizGame || !quizSelection) return;
-+
-+        quizSelection.style.display = 'none';
-+        quizGame.style.display = 'block';
-+
-+        const questao = quiz.questoes[questionIndex];
-+
-+        const quizTitle = document.getElementById('quiz-title');
-+        if (quizTitle) quizTitle.textContent = `${quiz.materia} - ${quiz.unidade}`;
-+
-+        const quizProgress = document.getElementById('quiz-progress');
-+        if (quizProgress) quizProgress.textContent = `Questão ${questionIndex + 1} de ${quiz.questoes.length}`;
-+
-+        const xpReward = document.getElementById('xp-reward');
-+        if (xpReward) xpReward.textContent = `+${quiz.ganhoXpPorQuestao} XP`;
-+
-+        const hintCost = document.getElementById('hint-cost');
-+        if (hintCost) hintCost.textContent = quiz.perdaXpDica;
-+
-+        const questionText = document.getElementById('question-text');
-+        if (questionText) questionText.textContent = questao.enunciado;
-+
-+        const optionsContainer = document.getElementById('options-container');
-+        if (optionsContainer) {
-+            optionsContainer.innerHTML = '';
-+            questao.alternativas.forEach((alternativa, index) => {
-+                const optionElement = document.createElement('div');
-+                optionElement.className = 'option';
-+                optionElement.setAttribute('data-option-index', index);
-+                const letra = String.fromCharCode(65 + index);
-+                optionElement.textContent = `${letra}) ${alternativa}`;
-+                optionsContainer.appendChild(optionElement);
-+            });
-+        }
-+
-+        const prevBtn = document.getElementById('prev-btn');
-+        const nextBtn = document.getElementById('next-btn');
-+        const submitBtn = document.getElementById('submit-btn');
-+
-+        if (prevBtn) prevBtn.style.display = questionIndex > 0 ? 'inline-flex' : 'none';
-+        if (nextBtn) nextBtn.style.display = questionIndex < quiz.questoes.length - 1 ? 'inline-flex' : 'none';
-+        if (submitBtn) submitBtn.style.display = questionIndex === quiz.questoes.length - 1 ? 'inline-flex' : 'none';
-+    },
-+
-+    renderQuizResults(quiz, xpGanhoTotal, xpTotal) {
-+        const quizGame = document.getElementById('quiz-game');
-+        const quizResults = document.getElementById('quiz-results');
-+        if (!quizGame || !quizResults) return;
-+
-+        quizGame.style.display = 'none';
-+        quizResults.style.display = 'block';
-+
-+        const resultsTitle = document.getElementById('results-title');
-+        const resultsDescription = document.getElementById('results-description');
-+        const resultsXp = document.getElementById('results-xp');
-+        const resultsTotalXp = document.getElementById('results-total-xp');
-+
-+        if (resultsTitle) resultsTitle.textContent = 'Parabéns!';
-+        if (resultsDescription) resultsDescription.textContent = `Você completou o quiz de ${quiz.materia}`;
-+        if (resultsXp) resultsXp.textContent = `+${xpGanhoTotal} XP`;
-+        if (resultsTotalXp) resultsTotalXp.textContent = xpTotal.toLocaleString('pt-BR');
-+    },
-+
-+    async renderProgress(user) {
-+        const progress = await EduGameAPI.getProgress(user.username);
-+
-+        const atividadeSemanal = document.getElementById('atividade-semanal');
-+        if (atividadeSemanal) {
-+            atividadeSemanal.textContent = `Você completou ${progress.atividadesSemana} atividades esta semana`;
-+        }
-+
-+        const materiasContainer = document.getElementById('materias-container');
-+        if (materiasContainer) {
-+            materiasContainer.innerHTML = '';
-+            progress.materias.forEach(materia => {
-+                materiasContainer.innerHTML += `
-+                    <div style="margin-bottom: 15px;">
-+                        <div style="display: flex; justify-content: space-between; margin-bottom: 5px;">
-+                            <span>${materia.nome}</span>
-+                            <span>${materia.percentual}%</span>
-+                        </div>
-+                        <div class="progress-bar">
-+                            <div class="progress-fill" style="width: ${materia.percentual}%"></div>
-+                        </div>
-+                        <div style="font-size: 0.9rem; color: var(--gray); margin-top: 5px;">
-+                            ${materia.xp} XP acumulados
-+                        </div>
-+                    </div>
-+                `;
-+            });
-+        }
-+
-+        const avatarContainer = document.getElementById('avatar-container');
-+        if (avatarContainer) {
-+            avatarContainer.innerHTML = `
-+                <div style="text-align: center;">
-+                    <div style="width: 120px; height: 120px; background-color: var(--secondary); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 3rem; color: white; margin: 0 auto 15px;">
-+                        <i class="fas fa-robot"></i>
-+                    </div>
-+                    <h4>Nível ${progress.avatar.nivel}</h4>
-+                    <p>${progress.avatar.titulo}</p>
-+                </div>
-+                
-+                <div style="flex: 1; min-width: 300px;">
-+                    <p style="margin-bottom: 15px;">Seu avatar ganhou novos itens com base no seu desempenho:</p>
-+                    <ul style="list-style-position: inside; margin-bottom: 15px;">
-+                        ${progress.avatar.itens.map(item => `<li>${item}</li>`).join('')}
-+                    </ul>
-+                    <p>Continue aprendendo para desbloquear mais itens e evoluir seu avatar!</p>
-+                </div>
-+            `;
-+        }
-+    },
-+
-+    async renderReports(user) {
-+        const reports = await EduGameAPI.getReports(user.username);
-+        const reportsContainer = document.getElementById('reports-container');
-+        const reportsSubtitle = document.getElementById('reports-subtitle');
-+        const exportDescription = document.getElementById('export-description');
-+
-+        if (!reportsContainer) return;
-+
-+        if (reportsSubtitle) {
-+            if (user.role === ROLES.PROFESSOR) {
-+                reportsSubtitle.textContent = 'Análises detalhadas do desempenho das turmas';
-+            } else if (user.role === ROLES.GESTOR) {
-+                reportsSubtitle.textContent = 'Visão consolidada de desempenho da rede escolar';
-+            } else {
-+                reportsSubtitle.textContent = 'Dados para apoiar seu aprendizado';
-+            }
-+        }
-+
-+        if (exportDescription) {
-+            if (user.role === ROLES.PROFESSOR || user.role === ROLES.GESTOR) {
-+                exportDescription.textContent = 'Exporte relatórios detalhados para análise pedagógica e tomada de decisão.';
-+            } else {
-+                exportDescription.textContent = 'Você pode compartilhar esses dados com seu professor para acompanhamento.';
-+            }
-+        }
-+
-+        let reportsHTML = '';
-+
-+        if (user.role === ROLES.ALUNO || user.role === ROLES.ALUNA) {
-+            reportsHTML = `
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-users"></i> Desempenho da Turma</h3>
-+                    <p>Média de acertos por aluno</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de desempenho da turma</p>
-+                    </div>
-+                    <p style="margin-top: 15px;">A turma tem média de ${reports.desempenhoTurma.mediaAcertos}% de acertos nos quizzes.</p>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-book-open"></i> Tópicos com Dificuldade</h3>
-+                    <p>Identificados por Machine Learning</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de tópicos com dificuldade</p>
-+                    </div>
-+                    <p style="margin-top: 15px;">${reports.topicosDificuldade.join(', ')} têm as maiores taxas de erro.</p>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-calendar-check"></i> Engajamento Temporal</h3>
-+                    <p>Atividade dos alunos ao longo do tempo</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de engajamento temporal</p>
-+                    </div>
-+                    <p style="margin-top: 15px;">${reports.engajamento.destaque}</p>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-trophy"></i> Ranking por XP</h3>
-+                    <p>Top 5 alunos da turma</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de ranking por XP</p>
-+                    </div>
-+                    <div style="margin-top: 15px;">
-+                        ${reports.rankingXp.top5.map((aluno, index) => `
-+                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px; padding: 5px; background-color: ${index < 3 ? '#E8F5E9' : '#f5f5f5'}; border-radius: 4px;">
-+                                <span>${index + 1}º ${aluno.nome}</span>
-+                                <span>${aluno.xp.toLocaleString('pt-BR')} XP</span>
-+                            </div>
-+                        `).join('')}
-+                    </div>
-+                </div>
-+            `;
-+        } else if (user.role === ROLES.PROFESSOR) {
-+            reportsHTML = `
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-chart-line"></i> Desempenho por Turma</h3>
-+                    <p>Análise comparativa das turmas</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de desempenho por turma</p>
-+                    </div>
-+                    <div style="margin-top: 15px;">
-+                        <p><strong>Média geral:</strong> ${reports.desempenhoTurma.mediaAcertos}% de acertos</p>
-+                        <p><strong>Maior acerto:</strong> ${reports.desempenhoTurma.topicoMaisAcertado}</p>
-+                        <p><strong>Maior dificuldade:</strong> ${reports.desempenhoTurma.topicoMenosAcertado}</p>
-+                    </div>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-lightbulb"></i> Insights do Machine Learning</h3>
-+                    <p>Recomendações para sua prática docente</p>
-+                    <div style="margin-top: 15px;">
-+                        ${reports.insightsProfessor ? reports.insightsProfessor.map(insight => `
-+                            <div style="background: #E3F2FD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--secondary);">
-+                                <i class="fas fa-chart-bar" style="color: var(--secondary); margin-right: 8px;"></i>
-+                                ${insight}
-+                            </div>
-+                        `).join('') : ''}
-+                    </div>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-bullseye"></i> Recomendações Pedagógicas</h3>
-+                    <p>Ações sugeridas pelo sistema</p>
-+                    <div style="margin-top: 15px;">
-+                        ${reports.recomendacoesML ? reports.recomendacoesML.map(recomendacao => `
-+                            <div style="background: #FFF3CD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--accent);">
-+                                <i class="fas fa-exclamation-circle" style="color: var(--accent); margin-right: 8px;"></i>
-+                                ${recomendacao}
-+                            </div>
-+                        `).join('') : ''}
-+                    </div>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-chart-pie"></i> Engajamento da Plataforma</h3>
-+                    <p>Estatísticas de uso dos alunos</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de engajamento da plataforma</p>
-+                    </div>
-+                    <div style="margin-top: 15px;">
-+                        <p><strong>Pico de uso:</strong> ${reports.engajamento.picoHorario}</p>
-+                        <p><strong>Taxa de uso semanal:</strong> ${reports.engajamento.taxaUso}</p>
-+                        <p><strong>Destaque:</strong> ${reports.engajamento.destaque}</p>
-+                    </div>
-+                </div>
-+            `;
-+        } else if (user.role === ROLES.GESTOR) {
-+            reportsHTML = `
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-school"></i> Visão Geral da Rede</h3>
-+                    <p>Indicadores consolidados de aprendizagem</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de desempenho por escola/turma</p>
-+                    </div>
-+                    <div style="margin-top: 15px;">
-+                        <p><strong>Média geral de acertos:</strong> ${reports.desempenhoTurma.mediaAcertos}%</p>
-+                        <p><strong>Áreas fortes:</strong> ${reports.desempenhoTurma.topicoMaisAcertado}</p>
-+                        <p><strong>Áreas críticas:</strong> ${reports.desempenhoTurma.topicoMenosAcertado}</p>
-+                    </div>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-users"></i> Alunos em Destaque e em Risco</h3>
-+                    <p>Baseado em XP acumulado</p>
-+                    <div class="chart-placeholder">
-+                        <p>Gráfico de distribuição de XP</p>
-+                    </div>
-+                    <div style="margin-top: 15px;">
-+                        <p><strong>Top 5 por XP:</strong></p>
-+                        ${reports.rankingXp.top5.map((aluno, index) => `
-+                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px; padding: 5px; background-color: ${index < 3 ? '#E8F5E9' : '#f5f5f5'}; border-radius: 4px;">
-+                                <span>${index + 1}º ${aluno.nome}</span>
-+                                <span>${aluno.xp.toLocaleString('pt-BR')} XP</span>
-+                            </div>
-+                        `).join('')}
-+                        <p style="margin-top: 10px; font-size: 0.9rem; color: var(--gray);">
-+                            Alunos com XP muito abaixo da média podem ser considerados em risco de aprendizagem.
-+                        </p>
-+                    </div>
-+                </div>
-+                
-+                <div class="chart-container">
-+                    <h3><i class="fas fa-lightbulb"></i> Insights para Gestão</h3>
-+                    <p>Pontos de atenção para políticas educacionais</p>
-+                    <div style="margin-top: 15px;">
-+                        ${reports.insightsProfessor ? reports.insightsProfessor.map(insight => `
-+                            <div style="background: #E3F2FD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--secondary);">
-+                                <i class="fas fa-chart-bar" style="color: var(--secondary); margin-right: 8px;"></i>
-+                                ${insight}
-+                            </div>
-+                        `).join('') : ''}
-+                        ${reports.recomendacoesML ? reports.recomendacoesML.map(recomendacao => `
-+                            <div style="background: #FFF3CD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--accent);">
-+                                <i class="fas fa-exclamation-circle" style="color: var(--accent); margin-right: 8px;"></i>
-+                                ${recomendacao}
-+                            </div>
-+                        `).join('') : ''}
-+                    </div>
-+                    <p style="margin-top: 15px; font-size: 0.85rem; color: var(--gray);">
-+                        As recomendações são baseadas em padrões de acertos, erros e engajamento.
-+                        Nesta versão MVP utilizamos regras heurísticas, mas a arquitetura já está preparada para integrar modelos de Machine Learning reais.
-+                    </p>
-+                </div>
-+            `;
-+        }
-+
-+        reportsContainer.innerHTML = reportsHTML;
-+    }
-+};
-+
-+/* ===========================================
-+   EVENTOS / CONTROLE
-+   =========================================== */
-+const EventHandlers = {
-+    navLinks: [],
-+
-+    init() {
-+        const loginBtn = document.getElementById('login-btn');
-+        const logoutBtn = document.getElementById('logout-btn');
-+
-+        if (loginBtn) loginBtn.addEventListener('click', () => this.handleLogin());
-+        if (logoutBtn) logoutBtn.addEventListener('click', () => this.handleLogout());
-+
-+        document.querySelectorAll('.user-type-btn').forEach(btn => {
-+            btn.addEventListener('click', (e) => {
-+                document.querySelectorAll('.user-type-btn').forEach(b => b.classList.remove('active'));
-+                e.currentTarget.classList.add('active');
-+            });
-+        });
-+
-+        this.navLinks = Array.from(document.querySelectorAll('.nav-link, .footer-nav'));
-+        this.navLinks.forEach(link => {
-+            link.addEventListener('click', (e) => {
-+                e.preventDefault();
-+                const page = link.getAttribute('data-page');
-+                this.navigateTo(page);
-+            });
-+        });
-+
-+        this.setupQuizHandlers();
-+
-+        const exportPdf = document.getElementById('export-pdf');
-+        const exportExcel = document.getElementById('export-excel');
-+        const refreshReports = document.getElementById('refresh-reports');
-+
-+        if (exportPdf) exportPdf.addEventListener('click', () => {
-+            UI.showNotification('Relatório PDF gerado com sucesso! (simulação)', 'success');
-+        });
-+
-+        if (exportExcel) exportExcel.addEventListener('click', () => {
-+            UI.showNotification('Planilha Excel exportada com sucesso! (simulação)', 'success');
-+        });
-+
-+        if (refreshReports) refreshReports.addEventListener('click', async () => {
-+            if (!AppState.userData) return;
-+            UI.showNotification('Atualizando dados...', 'warning');
-+            await AppState.refreshDashboard();
-+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+            await Render.renderReports(AppState.userData);
-+            UI.showNotification('Dados atualizados com sucesso!', 'success');
-+        });
-+
-+        const playAgainBtn = document.getElementById('play-again-btn');
-+        if (playAgainBtn) playAgainBtn.addEventListener('click', () => {
-+            this.navigateTo('quiz-play');
-+            const sel = document.getElementById('quiz-selection');
-+            const game = document.getElementById('quiz-game');
-+            const results = document.getElementById('quiz-results');
-+            if (sel) sel.style.display = 'block';
-+            if (game) game.style.display = 'none';
-+            if (results) results.style.display = 'none';
-+        });
-+
-+        const usernameSelect = document.getElementById('username');
-+        if (usernameSelect) usernameSelect.value = 'joao';
-+
-+        UI.showScreen('login-screen');
-+
-+        console.log('MVP EduGame - Demo Pronto!');
-+        console.log('Usuários disponíveis:');
-+        console.log('- joao (aluno)');
-+        console.log('- maria (aluna)');
-+        console.log('- prof_carlos (professor)');
-+        console.log('- gestor_ana (gestor)');
-+        console.log('Senha para todos: 123456');
-+    },
-+
-+    async handleLogin() {
-+        const username = document.getElementById('username').value;
-+        const password = document.getElementById('password').value;
-+
-+        UI.showLoading(true);
-+
-+        try {
-+            const result = await EduGameAPI.login(username, password);
-+            if (!result.success) {
-+                UI.showNotification(result.message || 'Erro no login', 'error');
-+                return;
-+            }
-+
-+            const ok = await AppState.init(username);
-+            if (!ok) {
-+                UI.showNotification('Erro ao carregar dados do usuário', 'error');
-+                return;
-+            }
-+
-+            Render.renderHeader(AppState.userData);
-+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+            Render.renderQuizzesList(AppState.quizzes, AppState.userData.role);
-+            UI.updateNavigation(AppState.userData.role);
-+
-+            UI.showScreen('app');
-+            const startPage = (AppState.userData.role === ROLES.GESTOR) ? 'reports' : 'dashboard';
-+            this.navigateTo(startPage);
-+
-+
-+            UI.showNotification(`Bem-vindo, ${AppState.userData.nome}!`, 'success');
-+        } catch (e) {
-+            console.error('Erro no login:', e);
-+            UI.showNotification('Erro ao conectar com o servidor', 'error');
-+        } finally {
-+            UI.showLoading(false);
-+        }
-+    },
-+
-+    async handleLogout() {
-+        if (AppState.currentUser) {
-+            await EduGameAPI.logout(AppState.currentUser);
-+        }
-+        AppState.reset();
-+        UI.showScreen('login-screen');
-+        UI.showNotification('Logout realizado com sucesso', 'success');
-+    },
-+
-+        async navigateTo(pageId) {
-+        if (!pageId) return;
-+
-+        // Destaca o item de menu ativo
-+        this.navLinks.forEach(link => {
-+            link.classList.toggle('active', link.getAttribute('data-page') === pageId);
-+        });
-+
-+        // Garante que o app esteja visível
-+        UI.showScreen('app');
-+
-+        // Esconde todas as páginas internas (Dashboard, Quizzes, Relatórios, etc.)
-+        const pages = document.querySelectorAll('#app .main-content .page');
-+        pages.forEach(page => {
-+            page.classList.remove('active');
-+            page.style.display = 'none';
-+        });
-+
-+        // Mostra apenas a página escolhida
-+        const pageElement = document.getElementById(pageId);
-+        if (pageElement) {
-+            pageElement.classList.add('active');
-+            pageElement.style.display = 'block';
-+            await this.loadPageData(pageId); // carrega dados específicos da página (progresso, relatórios etc.)
-+        }
-+
-+        // Reset visual do fluxo de quiz caso não esteja na página de jogar
-+        if (pageId !== 'quiz-play') {
-+            const sel = document.getElementById('quiz-selection');
-+            const game = document.getElementById('quiz-game');
-+            const results = document.getElementById('quiz-results');
-+            if (sel) sel.style.display = 'block';
-+            if (game) game.style.display = 'none';
-+            if (results) results.style.display = 'none';
-+        }
-+    },
-+
-+
-+    async loadPageData(pageId) {
-+        if (!AppState.currentUser) return;
-+
-+        if (pageId === 'progress') {
-+            await Render.renderProgress(AppState.userData);
-+        } else if (pageId === 'reports') {
-+            await Render.renderReports(AppState.userData);
-+        } else if (pageId === 'dashboard') {
-+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+        }
-+    },
-+
-+    setupQuizHandlers() {
-+        document.addEventListener('click', (e) => {
-+            const playBtn = e.target.closest('.btn-play-quiz');
-+            if (playBtn) {
-+                const quizId = parseInt(playBtn.getAttribute('data-quiz-id'), 10);
-+                this.startQuiz(quizId);
-+                return;
-+            }
-+
-+            const editBtn = e.target.closest('.btn-edit-quiz');
-+            if (editBtn) {
-+                const quizId = parseInt(editBtn.getAttribute('data-quiz-id'), 10);
-+                UI.showNotification(`Edição do quiz ${quizId} ainda não implementada (MVP).`, 'warning');
-+                return;
-+            }
-+
-+            const viewReportsBtn = e.target.closest('.btn-view-quiz-reports');
-+            if (viewReportsBtn) {
-+                const quizId = parseInt(viewReportsBtn.getAttribute('data-quiz-id'), 10);
-+                this.navigateTo('reports');
-+                UI.showNotification(`Exibindo visão consolidada dos relatórios (Quiz ID: ${quizId}).`, 'info');
-+                return;
-+            }
-+
-+            const option = e.target.closest('.option');
-+            if (option) {
-+                document.querySelectorAll('.option').forEach(opt => opt.classList.remove('selected'));
-+                option.classList.add('selected');
-+            }
-+        });
-+
-+        const hintBtn = document.getElementById('hint-btn');
-+        const nextBtn = document.getElementById('next-btn');
-+        const prevBtn = document.getElementById('prev-btn');
-+        const submitBtn = document.getElementById('submit-btn');
-+
-+        if (hintBtn) hintBtn.addEventListener('click', () => this.handleHint());
-+        if (nextBtn) nextBtn.addEventListener('click', () => this.handleNextQuestion());
-+        if (prevBtn) prevBtn.addEventListener('click', () => this.handlePrevQuestion());
-+        if (submitBtn) submitBtn.addEventListener('click', () => this.handleSubmitQuiz());
-+    },
-+
-+    async startQuiz(quizId) {
-+        if (!AppState.currentUser) {
-+            UI.showNotification('Faça login para jogar.', 'warning');
-+            return;
-+        }
-+
-+        UI.showLoading(true);
-+        try {
-+            const quiz = await EduGameAPI.getQuizById(quizId);
-+            if (!quiz) {
-+                UI.showNotification('Quiz não encontrado.', 'error');
-+                return;
-+            }
-+
-+            AppState.currentQuiz = quiz;
-+            AppState.currentQuestionIndex = 0;
-+            AppState.userAnswers = {};
-+
-+            this.navigateTo('quiz-play');
-+            Render.renderQuizGame(quiz, 0);
-+            UI.showNotification(`Quiz "${quiz.materia}" iniciado! Boa sorte!`, 'success');
-+        } catch (e) {
-+            console.error('Erro ao iniciar quiz:', e);
-+            UI.showNotification('Erro ao carregar quiz.', 'error');
-+        } finally {
-+            UI.showLoading(false);
-+        }
-+    },
-+
-+    async handleHint() {
-+        if (!AppState.currentQuiz || !AppState.currentUser) return;
-+
-+        const result = await EduGameAPI.consumirDica(AppState.currentUser, AppState.currentQuiz.id);
-+        const questao = AppState.currentQuiz.questoes[AppState.currentQuestionIndex];
-+
-+        alert(`Dica: ${questao.dica}\n\n-${result.custo} XP (custo da dica).\nXP atual: ${result.xpTotal} XP.`);
-+
-+        await AppState.refreshDashboard();
-+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+    },
-+
-+    async handleNextQuestion() {
-+        const selectedOption = document.querySelector('.option.selected');
-+        if (!selectedOption) {
-+            UI.showNotification('Por favor, selecione uma opção antes de continuar.', 'warning');
-+            return;
-+        }
-+
-+        const alternativaIndex = parseInt(selectedOption.getAttribute('data-option-index'), 10);
-+        const quiz = AppState.currentQuiz;
-+        const questao = quiz.questoes[AppState.currentQuestionIndex];
-+
-+        AppState.userAnswers[questao.id] = alternativaIndex;
-+
-+        const resultado = await EduGameAPI.submitAnswer({
-+            username: AppState.currentUser,
-+            quizId: quiz.id,
-+            questionId: questao.id,
-+            alternativaIndex
-+        });
-+
-+        if (resultado.correto) {
-+            UI.showNotification(`Resposta correta! +${resultado.xpGanho} XP!`, 'success');
-+        } else {
-+            const letraCorreta = String.fromCharCode(65 + resultado.respostaCorreta);
-+            UI.showNotification(`Resposta incorreta. A alternativa correta é ${letraCorreta}.`, 'error');
-+        }
-+
-+        await AppState.refreshDashboard();
-+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+
-+        if (AppState.currentQuestionIndex < quiz.questoes.length - 1) {
-+            AppState.currentQuestionIndex++;
-+            Render.renderQuizGame(quiz, AppState.currentQuestionIndex);
-+        } else {
-+            const nextBtn = document.getElementById('next-btn');
-+            const submitBtn = document.getElementById('submit-btn');
-+            if (nextBtn) nextBtn.style.display = 'none';
-+            if (submitBtn) submitBtn.style.display = 'inline-flex';
-+        }
-+    },
-+
-+    handlePrevQuestion() {
-+        if (!AppState.currentQuiz) return;
-+        if (AppState.currentQuestionIndex === 0) {
-+            UI.showNotification('Você já está na primeira questão.', 'info');
-+            return;
-+        }
-+        AppState.currentQuestionIndex--;
-+        Render.renderQuizGame(AppState.currentQuiz, AppState.currentQuestionIndex);
-+    },
-+
-+    async handleSubmitQuiz() {
-+        const selectedOption = document.querySelector('.option.selected');
-+        if (!selectedOption) {
-+            UI.showNotification('Por favor, selecione uma opção para a última questão.', 'warning');
-+            return;
-+        }
-+
-+        const alternativaIndex = parseInt(selectedOption.getAttribute('data-option-index'), 10);
-+        const quiz = AppState.currentQuiz;
-+        const questao = quiz.questoes[AppState.currentQuestionIndex];
-+
-+        AppState.userAnswers[questao.id] = alternativaIndex;
-+
-+        const resultado = await EduGameAPI.submitAnswer({
-+            username: AppState.currentUser,
-+            quizId: quiz.id,
-+            questionId: questao.id,
-+            alternativaIndex
-+        });
-+
-+        await EduGameAPI.completeQuiz(AppState.currentUser, quiz.id);
-+
-+        const xpGanhoTotal = quiz.questoes.length * quiz.ganhoXpPorQuestao;
-+
-+        await AppState.refreshDashboard();
-+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
-+
-+        const quizzes = await EduGameAPI.getQuizzes();
-+        AppState.quizzes = quizzes;
-+        Render.renderQuizzesList(quizzes, AppState.userData.role);
-+
-+        Render.renderQuizResults(quiz, xpGanhoTotal, resultado.xpTotal);
-+        UI.showNotification(`Quiz completado! Você ganhou ${xpGanhoTotal} XP!`, 'success');
-+    }
-+};
-+
-+/* ===========================================
-+   INICIALIZAÇÃO
-+   =========================================== */
-+document.addEventListener('DOMContentLoaded', () => {
-+    EventHandlers.init();
-+});
- 
-EOF
-)
+/* ===========================================
+   BACKEND SIMULADO (API FAKE)
+   =========================================== */
+const EduGameAPI = (() => {
+    const db = {
+        users: {
+            'joao': {
+                id: 1,
+                username: 'joao',
+                nome: 'João Silva',
+                sigla: 'JS',
+                role: 'aluno',
+                cidade: 'Vitória da Conquista, BA',
+                xp: 1850,
+                nivel: 3,
+                rankingTurma: 5,
+                totalAlunos: 32,
+                turma: '8º Ano A',
+                escola: 'Escola Municipal São Paulo'
+            },
+            'maria': {
+                id: 2,
+                username: 'maria',
+                nome: 'Maria Oliveira',
+                sigla: 'MO',
+                role: 'aluna',
+                cidade: 'Vitória da Conquista, BA',
+                xp: 2300,
+                nivel: 4,
+                rankingTurma: 2,
+                totalAlunos: 32,
+                turma: '8º Ano A',
+                escola: 'Escola Municipal São Paulo'
+            },
+            'prof_carlos': {
+                id: 3,
+                username: 'prof_carlos',
+                nome: 'Prof. Carlos Santos',
+                sigla: 'CS',
+                role: 'professor',
+                cidade: 'Vitória da Conquista, BA',
+                xp: 0,
+                nivel: 0,
+                turmas: ['8º Ano A', '9º Ano B', '7º Ano C'],
+                escola: 'Escola Municipal São Paulo'
+            },
+            'gestor_ana': {
+                id: 4,
+                username: 'gestor_ana',
+                nome: 'Ana Souza',
+                sigla: 'AS',
+                role: 'gestor',
+                cidade: 'Vitória da Conquista, BA',
+                xp: 0,
+                nivel: 0,
+                escola: 'Secretaria Municipal de Educação'
+            }
+        },
+
+        quizzes: [
+            {
+                id: 1,
+                materia: 'Matemática',
+                unidade: 'Unidade 3: Geometria',
+                descricao: 'Conceitos básicos de geometria plana',
+                dificuldade: 'Fácil',
+                ganhoXpPorQuestao: 50,
+                perdaXpDica: 10,
+                totalQuestoes: 3,
+                completado: false,
+                questoes: [
+                    {
+                        id: 1,
+                        enunciado: 'Qual é a fórmula para calcular a área de um triângulo?',
+                        alternativas: [
+                            'A = b × h',
+                            'A = (b × h) / 2',
+                            'A = π × r²',
+                            'A = l²'
+                        ],
+                        correta: 1,
+                        dica: 'A fórmula envolve base e altura, mas não é simplesmente a multiplicação das duas.'
+                    },
+                    {
+                        id: 2,
+                        enunciado: 'Um triângulo tem base de 10 cm e altura de 6 cm. Qual é sua área?',
+                        alternativas: [
+                            '60 cm²',
+                            '30 cm²',
+                            '15 cm²',
+                            '20 cm²'
+                        ],
+                        correta: 1,
+                        dica: 'Use a fórmula da área do triângulo: (base × altura) / 2'
+                    },
+                    {
+                        id: 3,
+                        enunciado: 'Qual é a soma dos ângulos internos de um triângulo?',
+                        alternativas: [
+                            '90º',
+                            '180º',
+                            '270º',
+                            '360º'
+                        ],
+                        correta: 1,
+                        dica: 'Pense na soma dos ângulos internos de qualquer triângulo.'
+                    }
+                ]
+            },
+            {
+                id: 2,
+                materia: 'Português',
+                unidade: 'Unidade 2: Análise Sintática',
+                descricao: 'Identificação de sujeito e predicado',
+                dificuldade: 'Médio',
+                ganhoXpPorQuestao: 75,
+                perdaXpDica: 15,
+                totalQuestoes: 3,
+                completado: true,
+                questoes: [
+                    {
+                        id: 1,
+                        enunciado: 'Na frase "O aluno estudou para a prova", qual é o sujeito?',
+                        alternativas: [
+                            'O aluno',
+                            'estudou',
+                            'para a prova',
+                            'prova'
+                        ],
+                        correta: 0,
+                        dica: 'O sujeito é quem pratica a ação do verbo.'
+                    }
+                ]
+            },
+            {
+                id: 3,
+                materia: 'Ciências',
+                unidade: 'Unidade 1: Sistema Solar',
+                descricao: 'Planetas e características do sistema solar',
+                dificuldade: 'Fácil',
+                ganhoXpPorQuestao: 50,
+                perdaXpDica: 10,
+                totalQuestoes: 4,
+                completado: false,
+                questoes: [
+                    {
+                        id: 1,
+                        enunciado: 'Qual é o maior planeta do sistema solar?',
+                        alternativas: [
+                            'Terra',
+                            'Júpiter',
+                            'Saturno',
+                            'Netuno'
+                        ],
+                        correta: 1,
+                        dica: 'É conhecido por sua grande mancha vermelha.'
+                    }
+                ]
+            }
+        ],
+
+        progresso: {
+            'joao': {
+                atividadesSemana: 12,
+                materias: [
+                    { nome: 'Matemática', percentual: 85, xp: 850 },
+                    { nome: 'Português', percentual: 72, xp: 600 },
+                    { nome: 'Ciências', percentual: 64, xp: 400 }
+                ],
+                avatar: {
+                    nivel: 3,
+                    titulo: 'Explorador do Conhecimento',
+                    itens: [
+                        'Capacete de bronze (completou 10 quizzes)',
+                        'Espada do saber (atingiu 1000 XP)',
+                        'Escudo da persistência (5 dias consecutivos de atividade)'
+                    ]
+                },
+                badges: [
+                    { id: 1, nome: 'Iniciante', icone: 'fas fa-rocket', desbloqueado: true },
+                    { id: 2, nome: 'Curioso', icone: 'fas fa-brain', desbloqueado: true },
+                    { id: 3, nome: 'Rápido', icone: 'fas fa-bolt', desbloqueado: true },
+                    { id: 4, nome: 'Mestre', icone: 'fas fa-crown', desbloqueado: false },
+                    { id: 5, nome: 'Estrela', icone: 'fas fa-star', desbloqueado: true },
+                    { id: 6, nome: 'Gênio', icone: 'fas fa-gem', desbloqueado: false }
+                ]
+            },
+            'maria': {
+                atividadesSemana: 18,
+                materias: [
+                    { nome: 'Matemática', percentual: 92, xp: 1200 },
+                    { nome: 'Português', percentual: 88, xp: 800 },
+                    { nome: 'Ciências', percentual: 78, xp: 300 }
+                ],
+                avatar: {
+                    nivel: 4,
+                    titulo: 'Mestre do Conhecimento',
+                    itens: [
+                        'Capacete de prata (completou 20 quizzes)',
+                        'Espada lendária (atingiu 2000 XP)',
+                        'Escudo da sabedoria (10 dias consecutivos de atividade)'
+                    ]
+                },
+                badges: [
+                    { id: 1, nome: 'Iniciante', icone: 'fas fa-rocket', desbloqueado: true },
+                    { id: 2, nome: 'Curioso', icone: 'fas fa-brain', desbloqueado: true },
+                    { id: 3, nome: 'Rápido', icone: 'fas fa-bolt', desbloqueado: true },
+                    { id: 4, nome: 'Mestre', icone: 'fas fa-crown', desbloqueado: true },
+                    { id: 5, nome: 'Estrela', icone: 'fas fa-star', desbloqueado: true },
+                    { id: 6, nome: 'Gênio', icone: 'fas fa-gem', desbloqueado: false }
+                ]
+            }
+        },
+
+        reports: {
+            desempenhoTurma: {
+                mediaAcertos: 78,
+                topicoMaisAcertado: 'Álgebra',
+                topicoMenosAcertado: 'Geometria'
+            },
+            topicosDificuldade: [
+                'Geometria',
+                'Frações',
+                'Análise Sintática'
+            ],
+            engajamento: {
+                destaque: 'Maior atividade às terças e quintas-feiras.',
+                picoHorario: '14h às 16h',
+                taxaUso: '85% dos alunos usam a plataforma semanalmente'
+            },
+            rankingXp: {
+                top5: [
+                    { nome: 'Carlos Mendes', xp: 2800 },
+                    { nome: 'Maria Oliveira', xp: 2300 },
+                    { nome: 'Ana Costa', xp: 2100 },
+                    { nome: 'Pedro Santos', xp: 1950 },
+                    { nome: 'João Silva', xp: 1850 }
+                ]
+            }
+        },
+
+        atividades: []
+    };
+
+    function delay(data, ms = 400) {
+        return new Promise(resolve => {
+            setTimeout(() => resolve(JSON.parse(JSON.stringify(data))), ms);
+        });
+    }
+
+    return {
+        login(username, password) {
+            if (password !== '123456') {
+                return delay({ success: false, message: 'Senha incorreta' });
+            }
+            const user = db.users[username];
+            if (!user) {
+                return delay({ success: false, message: 'Usuário não encontrado' });
+            }
+            db.atividades.push({ usuario: username, tipo: 'login', timestamp: new Date().toISOString() });
+            return delay({
+                success: true,
+                user: { ...user },
+                token: 'fake-jwt-' + Date.now()
+            });
+        },
+
+        logout(username) {
+            if (username) {
+                db.atividades.push({ usuario: username, tipo: 'logout', timestamp: new Date().toISOString() });
+            }
+            return delay({ success: true });
+        },
+
+        getUser(username) {
+            const user = db.users[username];
+            if (!user) return delay(null);
+            return delay({ ...user });
+        },
+
+        getDashboard(username) {
+            const user = db.users[username];
+            if (!user) return delay(null);
+            const progresso = db.progresso[username] || db.progresso['joao'];
+            return delay({
+                totalXp: user.xp,
+                nivelAtual: user.nivel,
+                xpProximoNivel: (user.nivel + 1) * 1000 - user.xp,
+                conquistasDesbloqueadas: progresso.badges.filter(b => b.desbloqueado).length,
+                conquistasTotal: progresso.badges.length,
+                quizCompletos: db.quizzes.filter(q => q.completado).length,
+                quizRestantes: db.quizzes.filter(q => !q.completado).length,
+                rankingPosicao: user.rankingTurma || 5,
+                rankingTotal: user.totalAlunos || 32,
+                distanciaProximoColocadoXp: 150
+            });
+        },
+
+        getQuizzes() {
+            return delay(db.quizzes);
+        },
+
+        getQuizById(id) {
+            const quiz = db.quizzes.find(q => q.id === id);
+            return delay(quiz ? { ...quiz } : null);
+        },
+
+        submitAnswer({ username, quizId, questionId, alternativaIndex }) {
+            const user = db.users[username];
+            const quiz = db.quizzes.find(q => q.id === quizId);
+            if (!user || !quiz) {
+                return delay({ correto: false, xpGanho: 0, xpTotal: user?.xp || 0 });
+            }
+            const questao = quiz.questoes.find(q => q.id === questionId);
+            if (!questao) {
+                return delay({ correto: false, xpGanho: 0, xpTotal: user.xp });
+            }
+            const correto = (questao.correta === alternativaIndex);
+            const xpGanho = correto ? quiz.ganhoXpPorQuestao : 0;
+            user.xp += xpGanho;
+
+            db.atividades.push({
+                usuario: username,
+                tipo: 'quiz_resposta',
+                quizId,
+                questionId,
+                correto,
+                xpGanho,
+                timestamp: new Date().toISOString()
+            });
+
+            return delay({
+                correto,
+                xpGanho,
+                xpTotal: user.xp,
+                respostaCorreta: questao.correta
+            });
+        },
+
+        consumirDica(username, quizId) {
+            const user = db.users[username];
+            const quiz = db.quizzes.find(q => q.id === quizId);
+            const custo = quiz ? quiz.perdaXpDica : 10;
+            if (user) {
+                user.xp = Math.max(0, user.xp - custo);
+                db.atividades.push({
+                    usuario: username,
+                    tipo: 'quiz_dica',
+                    quizId,
+                    custo,
+                    timestamp: new Date().toISOString()
+                });
+            }
+            return delay({ xpTotal: user?.xp || 0, custo });
+        },
+
+        getProgress(username) {
+            const progresso = db.progresso[username] || db.progresso['joao'];
+            return delay({ ...progresso });
+        },
+
+        getReports(username) {
+            const user = db.users[username];
+            let reports = { ...db.reports };
+
+            if (user?.role === 'professor' || user?.role === 'gestor') {
+                reports = {
+                    ...reports,
+                    insightsProfessor: [
+                        '35% dos alunos melhoraram o desempenho após usar gamificação',
+                        'Taxa de conclusão de quizzes aumentou 42%',
+                        'Alunos engajados têm 28% menos faltas'
+                    ],
+                    recomendacoesML: [
+                        'Revisar tópico de Geometria com turma 8º Ano A',
+                        'Incentivar uso da plataforma às segundas-feiras (menor engajamento)',
+                        'Criar quiz sobre Frações para reforço'
+                    ]
+                };
+            }
+            return delay(reports);
+        },
+
+        completeQuiz(username, quizId) {
+            const quiz = db.quizzes.find(q => q.id === quizId);
+            if (!quiz) return delay({ success: false });
+            quiz.completado = true;
+            db.atividades.push({
+                usuario: username,
+                tipo: 'quiz_completado',
+                quizId,
+                materia: quiz.materia,
+                timestamp: new Date().toISOString()
+            });
+            return delay({ success: true, quiz });
+        },
+
+        getRecentActivities(username, limit = 5) {
+            const atividades = db.atividades
+                .filter(a => a.usuario === username)
+                .sort((a, b) => new Date(b.timestamp) - new Date(a.timestamp))
+                .slice(0, limit);
+            return delay(atividades);
+        },
+
+        // Nova função "tipo ML": recomenda próximo foco para o aluno
+        getRecommendation(username) {
+            const progresso = db.progresso[username] || db.progresso['joao'];
+            const materiasOrdenadas = [...progresso.materias].sort((a, b) => a.percentual - b.percentual);
+            const materiaMaisFraca = materiasOrdenadas[0];
+
+            let mensagem = 'Você está indo muito bem!';
+            let acao = 'Continue praticando nos quizzes disponíveis.';
+
+            if (materiaMaisFraca) {
+                mensagem = `Seu ponto de atenção é ${materiaMaisFraca.nome}.`;
+                acao = `Recomendamos focar em quizzes de ${materiaMaisFraca.nome} para melhorar seu desempenho.`;
+            }
+
+            return delay({
+                materiaFoco: materiaMaisFraca?.nome || null,
+                mensagem,
+                acao
+            });
+        }
+    };
+})();
+
+/* ===========================================
+   PAPÉIS DE USUÁRIO
+   =========================================== */
+const ROLES = {
+    ALUNO: 'aluno',
+    ALUNA: 'aluna',
+    PROFESSOR: 'professor',
+    GESTOR: 'gestor'
+};
+
+/* ===========================================
+   GERENCIAMENTO DE ESTADO
+   =========================================== */
+const AppState = {
+    currentUser: null,
+    userData: null,
+    dashboard: null,
+    quizzes: [],
+    currentQuiz: null,
+    currentQuestionIndex: 0,
+    userAnswers: {},
+
+    async init(username) {
+        try {
+            const userData = await EduGameAPI.getUser(username);
+            this.currentUser = username;
+            this.userData = userData;
+
+            const [dashboard, quizzes] = await Promise.all([
+                EduGameAPI.getDashboard(username),
+                EduGameAPI.getQuizzes()
+            ]);
+
+            this.dashboard = dashboard;
+            this.quizzes = quizzes;
+            this.currentQuiz = quizzes.find(q => !q.completado) || quizzes[0] || null;
+            return true;
+        } catch (e) {
+            console.error('Erro ao inicializar AppState:', e);
+            return false;
+        }
+    },
+
+    reset() {
+        this.currentUser = null;
+        this.userData = null;
+        this.dashboard = null;
+        this.quizzes = [];
+        this.currentQuiz = null;
+        this.currentQuestionIndex = 0;
+        this.userAnswers = {};
+    },
+
+    async refreshDashboard() {
+        if (!this.currentUser) return;
+        this.dashboard = await EduGameAPI.getDashboard(this.currentUser);
+        this.userData = await EduGameAPI.getUser(this.currentUser);
+    }
+};
+
+/* ===========================================
+   UI / UTILITÁRIOS VISUAIS
+   =========================================== */
+const UI = {
+    showNotification(message, type = 'success', duration = 3000) {
+        const existing = document.querySelector('.notification');
+        if (existing) existing.remove();
+
+        const notification = document.createElement('div');
+        notification.className = `notification ${type}`;
+        notification.setAttribute('role', 'alert');
+        notification.setAttribute('aria-live', 'assertive');
+        notification.innerHTML = `
+            <div style="display: flex; align-items: flex-start; gap: 10px;">
+                <div style="font-size: 1.2rem;">
+                    ${type === 'success' ? '✓' : type === 'error' ? '✗' : '!'}
+                </div>
+                <div>${message}</div>
+            </div>
+        `;
+        document.body.appendChild(notification);
+
+        setTimeout(() => {
+            if (notification.parentNode) {
+                notification.parentNode.removeChild(notification);
+            }
+        }, duration);
+    },
+
+    showLoading(show) {
+        const loadingEl = document.getElementById('loading');
+        if (!loadingEl) return;
+        if (show) {
+            loadingEl.classList.add('active');
+        } else {
+            loadingEl.classList.remove('active');
+        }
+    },
+
+    // Alterna apenas entre tela de login e app
+    showScreen(screenId) {
+        const login = document.getElementById('login-screen');
+        const app = document.getElementById('app');
+
+        if (login) {
+            login.style.display = (screenId === 'login-screen') ? 'block' : 'none';
+        }
+        if (app) {
+            app.style.display = (screenId === 'app') ? 'block' : 'none';
+        }
+    },
+
+    // Menu diferente por papel
+    updateNavigation(role) {
+        const teacherNav = document.getElementById('teacher-nav');
+        const navItems = {
+            dashboard: document.querySelector('a.nav-link[data-page="dashboard"]')?.parentElement,
+            quizzes: document.querySelector('a.nav-link[data-page="quizzes"]')?.parentElement,
+            quizPlay: document.querySelector('a.nav-link[data-page="quiz-play"]')?.parentElement,
+            progress: document.querySelector('a.nav-link[data-page="progress"]')?.parentElement,
+            reports: document.querySelector('a.nav-link[data-page="reports"]')?.parentElement,
+            teacher: teacherNav
+        };
+
+        Object.values(navItems).forEach(li => {
+            if (li) li.style.display = '';
+        });
+
+        if (role === ROLES.ALUNO || role === ROLES.ALUNA) {
+            if (navItems.teacher) navItems.teacher.style.display = 'none';
+        } else if (role === ROLES.PROFESSOR) {
+            if (navItems.teacher) navItems.teacher.style.display = '';
+        } else if (role === ROLES.GESTOR) {
+            if (navItems.quizzes) navItems.quizzes.style.display = 'none';
+            if (navItems.quizPlay) navItems.quizPlay.style.display = 'none';
+            if (navItems.progress) navItems.progress.style.display = 'none';
+            if (navItems.teacher) navItems.teacher.style.display = '';
+        }
+    }
+};
+
+/* ===========================================
+   RENDERIZAÇÃO
+   =========================================== */
+const Render = {
+    renderHeader(user) {
+        const avatar = document.getElementById('user-avatar');
+        const name = document.getElementById('user-name');
+        if (avatar) avatar.textContent = user.sigla || user.nome.substring(0, 2).toUpperCase();
+        if (name) name.textContent = user.nome;
+
+        const subtitle = document.getElementById('dashboard-subtitle');
+        if (subtitle) {
+            if (user.role === ROLES.PROFESSOR) {
+                subtitle.textContent = `Olá, ${user.nome}. Acompanhe o desempenho das suas turmas.`;
+            } else if (user.role === ROLES.GESTOR) {
+                subtitle.textContent = `Olá, ${user.nome}. Veja os indicadores para tomada de decisão.`;
+            } else {
+                subtitle.textContent = `Olá, ${user.nome}. Vamos avançar no seu aprendizado?`;
+            }
+        }
+    },
+
+        async renderDashboard(dashboard, user) {
+        const role = user.role;
+        const cardsContainer = document.querySelector('.dashboard-cards');
+
+        // ============================
+        // DASHBOARD DE PROFESSOR
+        // ============================
+        if (role === ROLES.PROFESSOR && cardsContainer) {
+            // Esconde elementos típicos de aluno
+            const recCard = document.getElementById('recomendacao-card');
+            if (recCard) recCard.style.display = 'none';
+            const badgesContainer = document.getElementById('badges-container');
+            if (badgesContainer) badgesContainer.style.display = 'none';
+
+            const turmasAtivas = Array.isArray(user.turmas) ? user.turmas.length : 0;
+
+            cardsContainer.innerHTML = `
+                <div class="card">
+                    <h3><i class="fas fa-users"></i> Minhas turmas</h3>
+                    <div class="stat">${turmasAtivas}</div>
+                    <p>Turmas acompanhadas na plataforma</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 75%"></div>
+                    </div>
+                    <p>Meta: ampliar o uso da plataforma em todas as turmas.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-question-circle"></i> Quizzes ativos</h3>
+                    <div class="stat">15</div>
+                    <p>Quizzes disponíveis para os alunos</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 60%"></div>
+                    </div>
+                    <p>Use o painel do professor para criar e ajustar quizzes.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-chart-line"></i> Desempenho médio</h3>
+                    <div class="stat">78%</div>
+                    <p>Média de acertos das turmas</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 78%"></div>
+                    </div>
+                    <p>Meta: chegar a 85% de acertos.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-bell"></i> Pontos de atenção</h3>
+                    <p><strong>Conteúdos com maior dificuldade:</strong></p>
+                    <ul style="margin-top:10px; padding-left:18px;">
+                        <li>Geometria (8º Ano A)</li>
+                        <li>Frações (7º Ano C)</li>
+                    </ul>
+                    <p style="margin-top:10px;">Planeje revisões focadas usando os relatórios analíticos.</p>
+                </div>
+            `;
+
+            // Já ajustamos tudo para professor, não precisamos da lógica de aluno
+            return;
+        }
+
+        // ============================
+        // DASHBOARD DE GESTOR
+        // ============================
+        if (role === ROLES.GESTOR && cardsContainer) {
+            const recCard = document.getElementById('recomendacao-card');
+            if (recCard) recCard.style.display = 'none';
+            const badgesContainer = document.getElementById('badges-container');
+            if (badgesContainer) badgesContainer.style.display = 'none';
+
+            cardsContainer.innerHTML = `
+                <div class="card">
+                    <h3><i class="fas fa-school"></i> Escolas conectadas</h3>
+                    <div class="stat">12</div>
+                    <p>Unidades utilizando a plataforma</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 70%"></div>
+                    </div>
+                    <p>Meta: expandir o uso para toda a rede.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-users"></i> Engajamento dos alunos</h3>
+                    <div class="stat">85%</div>
+                    <p>Alunos que acessam a plataforma semanalmente</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 85%"></div>
+                    </div>
+                    <p>Priorizar escolas com engajamento abaixo de 60%.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-chart-line"></i> Desempenho da rede</h3>
+                    <div class="stat">78%</div>
+                    <p>Média geral de acertos em quizzes</p>
+                    <div class="progress-bar">
+                        <div class="progress-fill" style="width: 78%"></div>
+                    </div>
+                    <p>Foco em áreas críticas como Geometria e Frações.</p>
+                </div>
+
+                <div class="card">
+                    <h3><i class="fas fa-bullseye"></i> Prioridades estratégicas</h3>
+                    <ul style="margin-top:10px; padding-left:18px;">
+                        <li>Aumentar o uso da plataforma nas turmas finais do Fundamental.</li>
+                        <li>Monitorar risco de evasão via engajamento na plataforma.</li>
+                        <li>Planejar formações de professores com base nos dados.</li>
+                    </ul>
+                </div>
+            `;
+
+            return;
+        }
+
+        // ============================
+        // DASHBOARD DE ALUNO / ALUNA
+        // ============================
+        // Garante que os elementos "gamificados" estejam visíveis
+        const badgesContainer = document.getElementById('badges-container');
+        if (badgesContainer) badgesContainer.style.display = 'flex';
+        const recCard = document.getElementById('recomendacao-card');
+        if (recCard) recCard.style.display = '';
+
+        // XP Total
+        const xpElement = document.getElementById('total-xp');
+        if (xpElement) xpElement.textContent = `${dashboard.totalXp.toLocaleString('pt-BR')} XP`;
+
+        // Nível
+        const nivelElement = document.getElementById('nivel-text');
+        if (nivelElement) nivelElement.textContent = `Você está no nível ${dashboard.nivelAtual}`;
+
+        // Progresso para próximo nível
+        const totalParaProximo = dashboard.totalXp + dashboard.xpProximoNivel;
+        const xpPercent = Math.min(100, (dashboard.totalXp / totalParaProximo) * 100);
+
+        const xpProgress = document.getElementById('xp-progress');
+        if (xpProgress) xpProgress.style.width = `${xpPercent}%`;
+
+        const proximoElement = document.getElementById('proximo-nivel-text');
+        if (proximoElement) proximoElement.textContent = `${dashboard.xpProximoNivel} XP para o próximo nível`;
+
+        const xpText = document.getElementById('xp-text');
+        if (xpText) xpText.textContent = `${dashboard.totalXp.toLocaleString('pt-BR')} / ${totalParaProximo.toLocaleString('pt-BR')}`;
+
+        const xpBarFill = document.getElementById('xp-bar-fill');
+        if (xpBarFill) xpBarFill.style.width = `${xpPercent}%`;
+
+        // Conquistas
+        const conquistasStat = document.getElementById('conquistas-stat');
+        if (conquistasStat) conquistasStat.textContent = `${dashboard.conquistasDesbloqueadas}/${dashboard.conquistasTotal}`;
+
+        const conquistasProgress = document.getElementById('conquistas-progress');
+        if (conquistasProgress) {
+            const percentConq = Math.round((dashboard.conquistasDesbloqueadas / dashboard.conquistasTotal) * 100);
+            conquistasProgress.style.width = `${percentConq}%`;
+        }
+
+        // Quizzes
+        const quizCompletos = document.getElementById('quiz-completos');
+        if (quizCompletos) quizCompletos.textContent = dashboard.quizCompletos;
+
+        const quizRestantes = document.getElementById('quiz-restantes');
+        if (quizRestantes) quizRestantes.textContent = `${dashboard.quizRestantes} quiz restantes nesta unidade`;
+
+        // Ranking
+        const rankingPosicao = document.getElementById('ranking-posicao');
+        if (rankingPosicao) rankingPosicao.textContent = `#${dashboard.rankingPosicao}`;
+
+        const rankingTotal = document.getElementById('ranking-total');
+        if (rankingTotal) rankingTotal.textContent = `Entre ${dashboard.rankingTotal} alunos`;
+
+        const distanciaProximo = document.getElementById('distancia-proximo');
+        if (distanciaProximo) distanciaProximo.textContent = `${dashboard.distanciaProximoColocadoXp} XP atrás do ${dashboard.rankingPosicao}º lugar`;
+
+        // Gamificação: badges + recomendação "tipo ML"
+        await this.renderBadges(user);
+        await this.renderRecommendation(user);
+    }
+,
+
+    async renderBadges(user) {
+        const badgesContainer = document.getElementById('badges-container');
+        if (!badgesContainer) return;
+
+        const progress = await EduGameAPI.getProgress(user.username);
+        badgesContainer.innerHTML = '';
+
+        progress.badges.forEach(badge => {
+            const badgeElement = document.createElement('div');
+            badgeElement.className = `badge ${badge.desbloqueado ? '' : 'locked'}`;
+            badgeElement.innerHTML = `<i class="${badge.icone}"></i>`;
+            badgeElement.title = `${badge.nome} - ${badge.desbloqueado ? 'Desbloqueado' : 'Bloqueado'}`;
+            badgesContainer.appendChild(badgeElement);
+        });
+    },
+
+    // Card de recomendação “tipo ML”
+    async renderRecommendation(user) {
+        if (!(user.role === ROLES.ALUNO || user.role === ROLES.ALUNA)) {
+            const card = document.getElementById('recomendacao-card');
+            if (card) card.style.display = 'none';
+            return;
+        }
+        const rec = await EduGameAPI.getRecommendation(user.username);
+        const card = document.getElementById('recomendacao-card');
+        const msg = document.getElementById('recomendacao-mensagem');
+        const acao = document.getElementById('recomendacao-acao');
+        if (card && msg && acao && rec) {
+            msg.textContent = rec.mensagem;
+            acao.textContent = rec.acao;
+            card.style.display = 'block';
+        }
+    },
+
+    renderQuizzesList(quizzes, userRole) {
+        const quizzesList = document.getElementById('quizzes-list');
+        const playQuizList = document.getElementById('play-quiz-list');
+
+        const renderToElement = (element) => {
+            if (!element) return;
+            element.innerHTML = '';
+
+            if (!quizzes || quizzes.length === 0) {
+                element.innerHTML = `
+                    <div class="card">
+                        <h3><i class="fas fa-info-circle"></i> Nenhum quiz disponível</h3>
+                        <p>Peça ao seu professor para liberar novos quizzes ou revise os conteúdos já estudados.</p>
+                    </div>
+                `;
+                return;
+            }
+
+            quizzes.forEach(quiz => {
+                const quizCard = document.createElement('div');
+                quizCard.className = 'quiz-card';
+
+                const dificuldadeColor = {
+                    'Fácil': '#4CAF50',
+                    'Médio': '#FF9800',
+                    'Difícil': '#F44336'
+                }[quiz.dificuldade] || '#757575';
+
+                quizCard.innerHTML = `
+                    <h4>${quiz.materia}</h4>
+                    <p><strong>${quiz.unidade}</strong></p>
+                    <p style="margin: 10px 0;">${quiz.descricao}</p>
+                    <div class="quiz-meta">
+                        <div>
+                            <span style="display: inline-block; width: 10px; height: 10px; background-color: ${dificuldadeColor}; border-radius: 50%; margin-right: 5px;"></span>
+                            ${quiz.dificuldade}
+                        </div>
+                        <div>
+                            <i class="fas fa-star" style="color: #FFC107;"></i>
+                            ${quiz.ganhoXpPorQuestao} XP/questão
+                        </div>
+                    </div>
+                `;
+
+                const actionsWrapper = document.createElement('div');
+                actionsWrapper.style.marginTop = '15px';
+
+                const isAluno = (userRole === ROLES.ALUNO || userRole === ROLES.ALUNA);
+                const isProfessor = (userRole === ROLES.PROFESSOR);
+                const isGestor = (userRole === ROLES.GESTOR);
+
+                if ((isAluno || isProfessor) && quiz.completado) {
+                    actionsWrapper.innerHTML = `
+                        <div style="padding: 8px; background-color: #E8F5E9; border-radius: 4px; text-align: center; color: #2E7D32;">
+                            <i class="fas fa-check-circle"></i> Concluído
+                        </div>
+                    `;
+                } else {
+                    if (isAluno) {
+                        actionsWrapper.innerHTML = `
+                            <button class="btn btn-primary btn-play-quiz" data-quiz-id="${quiz.id}" style="width: 100%;">
+                                <i class="fas fa-play"></i> Jogar
+                            </button>
+                        `;
+                    } else if (isProfessor) {
+                        actionsWrapper.innerHTML = `
+                            <div style="display: flex; gap: 10px;">
+                                <button class="btn btn-primary btn-play-quiz" data-quiz-id="${quiz.id}" style="flex: 1;">
+                                    <i class="fas fa-play"></i> Visualizar/Jogar
+                                </button>
+                                <button class="btn btn-secondary btn-edit-quiz" data-quiz-id="${quiz.id}" style="flex: 1;">
+                                    <i class="fas fa-edit"></i> Editar
+                                </button>
+                            </div>
+                        `;
+                    } else if (isGestor) {
+                        actionsWrapper.innerHTML = `
+                            <button class="btn btn-secondary btn-view-quiz-reports" data-quiz-id="${quiz.id}" style="width: 100%;">
+                                <i class="fas fa-chart-bar"></i> Ver desempenho deste quiz
+                            </button>
+                        `;
+                    }
+                }
+
+                quizCard.appendChild(actionsWrapper);
+                element.appendChild(quizCard);
+            });
+        };
+
+        if (quizzesList) renderToElement(quizzesList);
+        if (playQuizList) renderToElement(playQuizList);
+    },
+
+    renderQuizGame(quiz, questionIndex) {
+        const quizGame = document.getElementById('quiz-game');
+        const quizSelection = document.getElementById('quiz-selection');
+        if (!quizGame || !quizSelection) return;
+
+        quizSelection.style.display = 'none';
+        quizGame.style.display = 'block';
+
+        const questao = quiz.questoes[questionIndex];
+
+        const quizTitle = document.getElementById('quiz-title');
+        if (quizTitle) quizTitle.textContent = `${quiz.materia} - ${quiz.unidade}`;
+
+        const quizProgress = document.getElementById('quiz-progress');
+        if (quizProgress) quizProgress.textContent = `Questão ${questionIndex + 1} de ${quiz.questoes.length}`;
+
+        const xpReward = document.getElementById('xp-reward');
+        if (xpReward) xpReward.textContent = `+${quiz.ganhoXpPorQuestao} XP`;
+
+        const hintCost = document.getElementById('hint-cost');
+        if (hintCost) hintCost.textContent = quiz.perdaXpDica;
+
+        const questionText = document.getElementById('question-text');
+        if (questionText) questionText.textContent = questao.enunciado;
+
+        const optionsContainer = document.getElementById('options-container');
+        if (optionsContainer) {
+            optionsContainer.innerHTML = '';
+            questao.alternativas.forEach((alternativa, index) => {
+                const optionElement = document.createElement('div');
+                optionElement.className = 'option';
+                optionElement.setAttribute('data-option-index', index);
+                const letra = String.fromCharCode(65 + index);
+                optionElement.textContent = `${letra}) ${alternativa}`;
+                optionsContainer.appendChild(optionElement);
+            });
+        }
+
+        const prevBtn = document.getElementById('prev-btn');
+        const nextBtn = document.getElementById('next-btn');
+        const submitBtn = document.getElementById('submit-btn');
+
+        if (prevBtn) prevBtn.style.display = questionIndex > 0 ? 'inline-flex' : 'none';
+        if (nextBtn) nextBtn.style.display = questionIndex < quiz.questoes.length - 1 ? 'inline-flex' : 'none';
+        if (submitBtn) submitBtn.style.display = questionIndex === quiz.questoes.length - 1 ? 'inline-flex' : 'none';
+    },
+
+    renderQuizResults(quiz, xpGanhoTotal, xpTotal) {
+        const quizGame = document.getElementById('quiz-game');
+        const quizResults = document.getElementById('quiz-results');
+        if (!quizGame || !quizResults) return;
+
+        quizGame.style.display = 'none';
+        quizResults.style.display = 'block';
+
+        const resultsTitle = document.getElementById('results-title');
+        const resultsDescription = document.getElementById('results-description');
+        const resultsXp = document.getElementById('results-xp');
+        const resultsTotalXp = document.getElementById('results-total-xp');
+
+        if (resultsTitle) resultsTitle.textContent = 'Parabéns!';
+        if (resultsDescription) resultsDescription.textContent = `Você completou o quiz de ${quiz.materia}`;
+        if (resultsXp) resultsXp.textContent = `+${xpGanhoTotal} XP`;
+        if (resultsTotalXp) resultsTotalXp.textContent = xpTotal.toLocaleString('pt-BR');
+    },
+
+    async renderProgress(user) {
+        const progress = await EduGameAPI.getProgress(user.username);
+
+        const atividadeSemanal = document.getElementById('atividade-semanal');
+        if (atividadeSemanal) {
+            atividadeSemanal.textContent = `Você completou ${progress.atividadesSemana} atividades esta semana`;
+        }
+
+        const materiasContainer = document.getElementById('materias-container');
+        if (materiasContainer) {
+            materiasContainer.innerHTML = '';
+            progress.materias.forEach(materia => {
+                materiasContainer.innerHTML += `
+                    <div style="margin-bottom: 15px;">
+                        <div style="display: flex; justify-content: space-between; margin-bottom: 5px;">
+                            <span>${materia.nome}</span>
+                            <span>${materia.percentual}%</span>
+                        </div>
+                        <div class="progress-bar">
+                            <div class="progress-fill" style="width: ${materia.percentual}%"></div>
+                        </div>
+                        <div style="font-size: 0.9rem; color: var(--gray); margin-top: 5px;">
+                            ${materia.xp} XP acumulados
+                        </div>
+                    </div>
+                `;
+            });
+        }
+
+        const avatarContainer = document.getElementById('avatar-container');
+        if (avatarContainer) {
+            avatarContainer.innerHTML = `
+                <div style="text-align: center;">
+                    <div style="width: 120px; height: 120px; background-color: var(--secondary); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 3rem; color: white; margin: 0 auto 15px;">
+                        <i class="fas fa-robot"></i>
+                    </div>
+                    <h4>Nível ${progress.avatar.nivel}</h4>
+                    <p>${progress.avatar.titulo}</p>
+                </div>
+                
+                <div style="flex: 1; min-width: 300px;">
+                    <p style="margin-bottom: 15px;">Seu avatar ganhou novos itens com base no seu desempenho:</p>
+                    <ul style="list-style-position: inside; margin-bottom: 15px;">
+                        ${progress.avatar.itens.map(item => `<li>${item}</li>`).join('')}
+                    </ul>
+                    <p>Continue aprendendo para desbloquear mais itens e evoluir seu avatar!</p>
+                </div>
+            `;
+        }
+    },
+
+    async renderReports(user) {
+        const reports = await EduGameAPI.getReports(user.username);
+        const reportsContainer = document.getElementById('reports-container');
+        const reportsSubtitle = document.getElementById('reports-subtitle');
+        const exportDescription = document.getElementById('export-description');
+
+        if (!reportsContainer) return;
+
+        if (reportsSubtitle) {
+            if (user.role === ROLES.PROFESSOR) {
+                reportsSubtitle.textContent = 'Análises detalhadas do desempenho das turmas';
+            } else if (user.role === ROLES.GESTOR) {
+                reportsSubtitle.textContent = 'Visão consolidada de desempenho da rede escolar';
+            } else {
+                reportsSubtitle.textContent = 'Dados para apoiar seu aprendizado';
+            }
+        }
+
+        if (exportDescription) {
+            if (user.role === ROLES.PROFESSOR || user.role === ROLES.GESTOR) {
+                exportDescription.textContent = 'Exporte relatórios detalhados para análise pedagógica e tomada de decisão.';
+            } else {
+                exportDescription.textContent = 'Você pode compartilhar esses dados com seu professor para acompanhamento.';
+            }
+        }
+
+        let reportsHTML = '';
+
+        if (user.role === ROLES.ALUNO || user.role === ROLES.ALUNA) {
+            reportsHTML = `
+                <div class="chart-container">
+                    <h3><i class="fas fa-users"></i> Desempenho da Turma</h3>
+                    <p>Média de acertos por aluno</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de desempenho da turma</p>
+                    </div>
+                    <p style="margin-top: 15px;">A turma tem média de ${reports.desempenhoTurma.mediaAcertos}% de acertos nos quizzes.</p>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-book-open"></i> Tópicos com Dificuldade</h3>
+                    <p>Identificados por Machine Learning</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de tópicos com dificuldade</p>
+                    </div>
+                    <p style="margin-top: 15px;">${reports.topicosDificuldade.join(', ')} têm as maiores taxas de erro.</p>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-calendar-check"></i> Engajamento Temporal</h3>
+                    <p>Atividade dos alunos ao longo do tempo</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de engajamento temporal</p>
+                    </div>
+                    <p style="margin-top: 15px;">${reports.engajamento.destaque}</p>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-trophy"></i> Ranking por XP</h3>
+                    <p>Top 5 alunos da turma</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de ranking por XP</p>
+                    </div>
+                    <div style="margin-top: 15px;">
+                        ${reports.rankingXp.top5.map((aluno, index) => `
+                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px; padding: 5px; background-color: ${index < 3 ? '#E8F5E9' : '#f5f5f5'}; border-radius: 4px;">
+                                <span>${index + 1}º ${aluno.nome}</span>
+                                <span>${aluno.xp.toLocaleString('pt-BR')} XP</span>
+                            </div>
+                        `).join('')}
+                    </div>
+                </div>
+            `;
+        } else if (user.role === ROLES.PROFESSOR) {
+            reportsHTML = `
+                <div class="chart-container">
+                    <h3><i class="fas fa-chart-line"></i> Desempenho por Turma</h3>
+                    <p>Análise comparativa das turmas</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de desempenho por turma</p>
+                    </div>
+                    <div style="margin-top: 15px;">
+                        <p><strong>Média geral:</strong> ${reports.desempenhoTurma.mediaAcertos}% de acertos</p>
+                        <p><strong>Maior acerto:</strong> ${reports.desempenhoTurma.topicoMaisAcertado}</p>
+                        <p><strong>Maior dificuldade:</strong> ${reports.desempenhoTurma.topicoMenosAcertado}</p>
+                    </div>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-lightbulb"></i> Insights do Machine Learning</h3>
+                    <p>Recomendações para sua prática docente</p>
+                    <div style="margin-top: 15px;">
+                        ${reports.insightsProfessor ? reports.insightsProfessor.map(insight => `
+                            <div style="background: #E3F2FD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--secondary);">
+                                <i class="fas fa-chart-bar" style="color: var(--secondary); margin-right: 8px;"></i>
+                                ${insight}
+                            </div>
+                        `).join('') : ''}
+                    </div>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-bullseye"></i> Recomendações Pedagógicas</h3>
+                    <p>Ações sugeridas pelo sistema</p>
+                    <div style="margin-top: 15px;">
+                        ${reports.recomendacoesML ? reports.recomendacoesML.map(recomendacao => `
+                            <div style="background: #FFF3CD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--accent);">
+                                <i class="fas fa-exclamation-circle" style="color: var(--accent); margin-right: 8px;"></i>
+                                ${recomendacao}
+                            </div>
+                        `).join('') : ''}
+                    </div>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-chart-pie"></i> Engajamento da Plataforma</h3>
+                    <p>Estatísticas de uso dos alunos</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de engajamento da plataforma</p>
+                    </div>
+                    <div style="margin-top: 15px;">
+                        <p><strong>Pico de uso:</strong> ${reports.engajamento.picoHorario}</p>
+                        <p><strong>Taxa de uso semanal:</strong> ${reports.engajamento.taxaUso}</p>
+                        <p><strong>Destaque:</strong> ${reports.engajamento.destaque}</p>
+                    </div>
+                </div>
+            `;
+        } else if (user.role === ROLES.GESTOR) {
+            reportsHTML = `
+                <div class="chart-container">
+                    <h3><i class="fas fa-school"></i> Visão Geral da Rede</h3>
+                    <p>Indicadores consolidados de aprendizagem</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de desempenho por escola/turma</p>
+                    </div>
+                    <div style="margin-top: 15px;">
+                        <p><strong>Média geral de acertos:</strong> ${reports.desempenhoTurma.mediaAcertos}%</p>
+                        <p><strong>Áreas fortes:</strong> ${reports.desempenhoTurma.topicoMaisAcertado}</p>
+                        <p><strong>Áreas críticas:</strong> ${reports.desempenhoTurma.topicoMenosAcertado}</p>
+                    </div>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-users"></i> Alunos em Destaque e em Risco</h3>
+                    <p>Baseado em XP acumulado</p>
+                    <div class="chart-placeholder">
+                        <p>Gráfico de distribuição de XP</p>
+                    </div>
+                    <div style="margin-top: 15px;">
+                        <p><strong>Top 5 por XP:</strong></p>
+                        ${reports.rankingXp.top5.map((aluno, index) => `
+                            <div style="display: flex; justify-content: space-between; margin-bottom: 5px; padding: 5px; background-color: ${index < 3 ? '#E8F5E9' : '#f5f5f5'}; border-radius: 4px;">
+                                <span>${index + 1}º ${aluno.nome}</span>
+                                <span>${aluno.xp.toLocaleString('pt-BR')} XP</span>
+                            </div>
+                        `).join('')}
+                        <p style="margin-top: 10px; font-size: 0.9rem; color: var(--gray);">
+                            Alunos com XP muito abaixo da média podem ser considerados em risco de aprendizagem.
+                        </p>
+                    </div>
+                </div>
+                
+                <div class="chart-container">
+                    <h3><i class="fas fa-lightbulb"></i> Insights para Gestão</h3>
+                    <p>Pontos de atenção para políticas educacionais</p>
+                    <div style="margin-top: 15px;">
+                        ${reports.insightsProfessor ? reports.insightsProfessor.map(insight => `
+                            <div style="background: #E3F2FD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--secondary);">
+                                <i class="fas fa-chart-bar" style="color: var(--secondary); margin-right: 8px;"></i>
+                                ${insight}
+                            </div>
+                        `).join('') : ''}
+                        ${reports.recomendacoesML ? reports.recomendacoesML.map(recomendacao => `
+                            <div style="background: #FFF3CD; padding: 12px; margin-bottom: 10px; border-radius: 6px; border-left: 4px solid var(--accent);">
+                                <i class="fas fa-exclamation-circle" style="color: var(--accent); margin-right: 8px;"></i>
+                                ${recomendacao}
+                            </div>
+                        `).join('') : ''}
+                    </div>
+                    <p style="margin-top: 15px; font-size: 0.85rem; color: var(--gray);">
+                        As recomendações são baseadas em padrões de acertos, erros e engajamento.
+                        Nesta versão MVP utilizamos regras heurísticas, mas a arquitetura já está preparada para integrar modelos de Machine Learning reais.
+                    </p>
+                </div>
+            `;
+        }
+
+        reportsContainer.innerHTML = reportsHTML;
+    }
+};
+
+/* ===========================================
+   EVENTOS / CONTROLE
+   =========================================== */
+const EventHandlers = {
+    navLinks: [],
+
+    init() {
+        const loginBtn = document.getElementById('login-btn');
+        const logoutBtn = document.getElementById('logout-btn');
+
+        if (loginBtn) loginBtn.addEventListener('click', () => this.handleLogin());
+        if (logoutBtn) logoutBtn.addEventListener('click', () => this.handleLogout());
+
+        document.querySelectorAll('.user-type-btn').forEach(btn => {
+            btn.addEventListener('click', (e) => {
+                document.querySelectorAll('.user-type-btn').forEach(b => b.classList.remove('active'));
+                e.currentTarget.classList.add('active');
+            });
+        });
+
+        this.navLinks = Array.from(document.querySelectorAll('.nav-link, .footer-nav'));
+        this.navLinks.forEach(link => {
+            link.addEventListener('click', (e) => {
+                e.preventDefault();
+                const page = link.getAttribute('data-page');
+                this.navigateTo(page);
+            });
+        });
+
+        this.setupQuizHandlers();
+
+        const exportPdf = document.getElementById('export-pdf');
+        const exportExcel = document.getElementById('export-excel');
+        const refreshReports = document.getElementById('refresh-reports');
+
+        if (exportPdf) exportPdf.addEventListener('click', () => {
+            UI.showNotification('Relatório PDF gerado com sucesso! (simulação)', 'success');
+        });
+
+        if (exportExcel) exportExcel.addEventListener('click', () => {
+            UI.showNotification('Planilha Excel exportada com sucesso! (simulação)', 'success');
+        });
+
+        if (refreshReports) refreshReports.addEventListener('click', async () => {
+            if (!AppState.userData) return;
+            UI.showNotification('Atualizando dados...', 'warning');
+            await AppState.refreshDashboard();
+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
+            await Render.renderReports(AppState.userData);
+            UI.showNotification('Dados atualizados com sucesso!', 'success');
+        });
+
+        const playAgainBtn = document.getElementById('play-again-btn');
+        if (playAgainBtn) playAgainBtn.addEventListener('click', () => {
+            this.navigateTo('quiz-play');
+            const sel = document.getElementById('quiz-selection');
+            const game = document.getElementById('quiz-game');
+            const results = document.getElementById('quiz-results');
+            if (sel) sel.style.display = 'block';
+            if (game) game.style.display = 'none';
+            if (results) results.style.display = 'none';
+        });
+
+        const usernameSelect = document.getElementById('username');
+        if (usernameSelect) usernameSelect.value = 'joao';
+
+        UI.showScreen('login-screen');
+
+        console.log('MVP EduGame - Demo Pronto!');
+        console.log('Usuários disponíveis:');
+        console.log('- joao (aluno)');
+        console.log('- maria (aluna)');
+        console.log('- prof_carlos (professor)');
+        console.log('- gestor_ana (gestor)');
+        console.log('Senha para todos: 123456');
+    },
+
+    async handleLogin() {
+        const username = document.getElementById('username').value;
+        const password = document.getElementById('password').value;
+
+        UI.showLoading(true);
+
+        try {
+            const result = await EduGameAPI.login(username, password);
+            if (!result.success) {
+                UI.showNotification(result.message || 'Erro no login', 'error');
+                return;
+            }
+
+            const ok = await AppState.init(username);
+            if (!ok) {
+                UI.showNotification('Erro ao carregar dados do usuário', 'error');
+                return;
+            }
+
+            Render.renderHeader(AppState.userData);
+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
+            Render.renderQuizzesList(AppState.quizzes, AppState.userData.role);
+            UI.updateNavigation(AppState.userData.role);
+
+            UI.showScreen('app');
+            const startPage = (AppState.userData.role === ROLES.GESTOR) ? 'reports' : 'dashboard';
+            this.navigateTo(startPage);
+
+
+            UI.showNotification(`Bem-vindo, ${AppState.userData.nome}!`, 'success');
+        } catch (e) {
+            console.error('Erro no login:', e);
+            UI.showNotification('Erro ao conectar com o servidor', 'error');
+        } finally {
+            UI.showLoading(false);
+        }
+    },
+
+    async handleLogout() {
+        if (AppState.currentUser) {
+            await EduGameAPI.logout(AppState.currentUser);
+        }
+        AppState.reset();
+        UI.showScreen('login-screen');
+        UI.showNotification('Logout realizado com sucesso', 'success');
+    },
+
+        async navigateTo(pageId) {
+        if (!pageId) return;
+
+        // Destaca o item de menu ativo
+        this.navLinks.forEach(link => {
+            link.classList.toggle('active', link.getAttribute('data-page') === pageId);
+        });
+
+        // Garante que o app esteja visível
+        UI.showScreen('app');
+
+        // Esconde todas as páginas internas (Dashboard, Quizzes, Relatórios, etc.)
+        const pages = document.querySelectorAll('#app .main-content .page');
+        pages.forEach(page => {
+            page.classList.remove('active');
+            page.style.display = 'none';
+        });
+
+        // Mostra apenas a página escolhida
+        const pageElement = document.getElementById(pageId);
+        if (pageElement) {
+            pageElement.classList.add('active');
+            pageElement.style.display = 'block';
+            await this.loadPageData(pageId); // carrega dados específicos da página (progresso, relatórios etc.)
+        }
+
+        // Reset visual do fluxo de quiz caso não esteja na página de jogar
+        if (pageId !== 'quiz-play') {
+            const sel = document.getElementById('quiz-selection');
+            const game = document.getElementById('quiz-game');
+            const results = document.getElementById('quiz-results');
+            if (sel) sel.style.display = 'block';
+            if (game) game.style.display = 'none';
+            if (results) results.style.display = 'none';
+        }
+    },
+
+
+    async loadPageData(pageId) {
+        if (!AppState.currentUser) return;
+
+        if (pageId === 'progress') {
+            await Render.renderProgress(AppState.userData);
+        } else if (pageId === 'reports') {
+            await Render.renderReports(AppState.userData);
+        } else if (pageId === 'dashboard') {
+            await Render.renderDashboard(AppState.dashboard, AppState.userData);
+        }
+    },
+
+    setupQuizHandlers() {
+        document.addEventListener('click', (e) => {
+            const playBtn = e.target.closest('.btn-play-quiz');
+            if (playBtn) {
+                const quizId = parseInt(playBtn.getAttribute('data-quiz-id'), 10);
+                this.startQuiz(quizId);
+                return;
+            }
+
+            const editBtn = e.target.closest('.btn-edit-quiz');
+            if (editBtn) {
+                const quizId = parseInt(editBtn.getAttribute('data-quiz-id'), 10);
+                UI.showNotification(`Edição do quiz ${quizId} ainda não implementada (MVP).`, 'warning');
+                return;
+            }
+
+            const viewReportsBtn = e.target.closest('.btn-view-quiz-reports');
+            if (viewReportsBtn) {
+                const quizId = parseInt(viewReportsBtn.getAttribute('data-quiz-id'), 10);
+                this.navigateTo('reports');
+                UI.showNotification(`Exibindo visão consolidada dos relatórios (Quiz ID: ${quizId}).`, 'info');
+                return;
+            }
+
+            const option = e.target.closest('.option');
+            if (option) {
+                document.querySelectorAll('.option').forEach(opt => opt.classList.remove('selected'));
+                option.classList.add('selected');
+            }
+        });
+
+        const hintBtn = document.getElementById('hint-btn');
+        const nextBtn = document.getElementById('next-btn');
+        const prevBtn = document.getElementById('prev-btn');
+        const submitBtn = document.getElementById('submit-btn');
+
+        if (hintBtn) hintBtn.addEventListener('click', () => this.handleHint());
+        if (nextBtn) nextBtn.addEventListener('click', () => this.handleNextQuestion());
+        if (prevBtn) prevBtn.addEventListener('click', () => this.handlePrevQuestion());
+        if (submitBtn) submitBtn.addEventListener('click', () => this.handleSubmitQuiz());
+    },
+
+    async startQuiz(quizId) {
+        if (!AppState.currentUser) {
+            UI.showNotification('Faça login para jogar.', 'warning');
+            return;
+        }
+
+        UI.showLoading(true);
+        try {
+            const quiz = await EduGameAPI.getQuizById(quizId);
+            if (!quiz) {
+                UI.showNotification('Quiz não encontrado.', 'error');
+                return;
+            }
+
+            AppState.currentQuiz = quiz;
+            AppState.currentQuestionIndex = 0;
+            AppState.userAnswers = {};
+
+            this.navigateTo('quiz-play');
+            Render.renderQuizGame(quiz, 0);
+            UI.showNotification(`Quiz "${quiz.materia}" iniciado! Boa sorte!`, 'success');
+        } catch (e) {
+            console.error('Erro ao iniciar quiz:', e);
+            UI.showNotification('Erro ao carregar quiz.', 'error');
+        } finally {
+            UI.showLoading(false);
+        }
+    },
+
+    async handleHint() {
+        if (!AppState.currentQuiz || !AppState.currentUser) return;
+
+        const result = await EduGameAPI.consumirDica(AppState.currentUser, AppState.currentQuiz.id);
+        const questao = AppState.currentQuiz.questoes[AppState.currentQuestionIndex];
+
+        alert(`Dica: ${questao.dica}\n\n-${result.custo} XP (custo da dica).\nXP atual: ${result.xpTotal} XP.`);
+
+        await AppState.refreshDashboard();
+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
+    },
+
+    async handleNextQuestion() {
+        const selectedOption = document.querySelector('.option.selected');
+        if (!selectedOption) {
+            UI.showNotification('Por favor, selecione uma opção antes de continuar.', 'warning');
+            return;
+        }
+
+        const alternativaIndex = parseInt(selectedOption.getAttribute('data-option-index'), 10);
+        const quiz = AppState.currentQuiz;
+        const questao = quiz.questoes[AppState.currentQuestionIndex];
+
+        AppState.userAnswers[questao.id] = alternativaIndex;
+
+        const resultado = await EduGameAPI.submitAnswer({
+            username: AppState.currentUser,
+            quizId: quiz.id,
+            questionId: questao.id,
+            alternativaIndex
+        });
+
+        if (resultado.correto) {
+            UI.showNotification(`Resposta correta! +${resultado.xpGanho} XP!`, 'success');
+        } else {
+            const letraCorreta = String.fromCharCode(65 + resultado.respostaCorreta);
+            UI.showNotification(`Resposta incorreta. A alternativa correta é ${letraCorreta}.`, 'error');
+        }
+
+        await AppState.refreshDashboard();
+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
+
+        if (AppState.currentQuestionIndex < quiz.questoes.length - 1) {
+            AppState.currentQuestionIndex++;
+            Render.renderQuizGame(quiz, AppState.currentQuestionIndex);
+        } else {
+            const nextBtn = document.getElementById('next-btn');
+            const submitBtn = document.getElementById('submit-btn');
+            if (nextBtn) nextBtn.style.display = 'none';
+            if (submitBtn) submitBtn.style.display = 'inline-flex';
+        }
+    },
+
+    handlePrevQuestion() {
+        if (!AppState.currentQuiz) return;
+        if (AppState.currentQuestionIndex === 0) {
+            UI.showNotification('Você já está na primeira questão.', 'info');
+            return;
+        }
+        AppState.currentQuestionIndex--;
+        Render.renderQuizGame(AppState.currentQuiz, AppState.currentQuestionIndex);
+    },
+
+    async handleSubmitQuiz() {
+        const selectedOption = document.querySelector('.option.selected');
+        if (!selectedOption) {
+            UI.showNotification('Por favor, selecione uma opção para a última questão.', 'warning');
+            return;
+        }
+
+        const alternativaIndex = parseInt(selectedOption.getAttribute('data-option-index'), 10);
+        const quiz = AppState.currentQuiz;
+        const questao = quiz.questoes[AppState.currentQuestionIndex];
+
+        AppState.userAnswers[questao.id] = alternativaIndex;
+
+        const resultado = await EduGameAPI.submitAnswer({
+            username: AppState.currentUser,
+            quizId: quiz.id,
+            questionId: questao.id,
+            alternativaIndex
+        });
+
+        await EduGameAPI.completeQuiz(AppState.currentUser, quiz.id);
+
+        const xpGanhoTotal = quiz.questoes.length * quiz.ganhoXpPorQuestao;
+
+        await AppState.refreshDashboard();
+        await Render.renderDashboard(AppState.dashboard, AppState.userData);
+
+        const quizzes = await EduGameAPI.getQuizzes();
+        AppState.quizzes = quizzes;
+        Render.renderQuizzesList(quizzes, AppState.userData.role);
+
+        Render.renderQuizResults(quiz, xpGanhoTotal, resultado.xpTotal);
+        UI.showNotification(`Quiz completado! Você ganhou ${xpGanhoTotal} XP!`, 'success');
+    }
+};
+
+/* ===========================================
+   INICIALIZAÇÃO
+   =========================================== */
+document.addEventListener('DOMContentLoaded', () => {
+    EventHandlers.init();
+});
 
EOF
)
