# Prototipa-AVA-Blackboard

# Botões Interativos & Linha do Tempo de Ações — AVA Senac

---

## 🔐 Login.html

**Botões e interações:**
- **AA Alterar tamanho do texto** → cicla entre 3 tamanhos de fonte (normal → médio → grande)
- **☀ Configurar contraste** → ativa/desativa modo alto contraste na página
- **👁 Ícone olho (senha)** → mostra ou oculta o texto da senha
- **Fazer login** → valida se os campos estão preenchidos, redireciona para `AVA.html`

**Linha do tempo de ações:**
```
1. Usuário acessa a página
2. (opcional) Ajusta tamanho do texto ou contraste
3. Digita usuário e senha
4. Clica em "Fazer login"
5. Sistema valida → redireciona para AVA.html
```

---

## 🏠 AVA.html (Home)

**Botões e interações:**
- **Rafael Rodrigues (avatar)** → navega para `PerfilUsuario.html`
- **Sala de Aula** → ancora na seção `#titulo-salas`
- **Linha do tempo** → navega para `LinhaTempo.html`
- **Fazer Logoff** → retorna para `Login.html`
- **⭐ Favoritar card** → alterna estrela preenchida/vazia (ativo/inativo)
- **Vários instrutores** → abre/fecha popover com lista de instrutores
- **Clique no card do curso** → navega para `SalaAula.html`

**Linha do tempo de ações:**
```
1. Usuário chega vindo do Login
2. Visualiza banner e tutorial
3. Pesquisa ou filtra cursos por categoria
4. (opcional) Favorita um curso
5. (opcional) Clica em "Vários instrutores" → vê o popover
6. Clica no card do curso → vai para SalaAula.html
```

---

## 📚 SalaAula.html

**Botões e interações:**
- **Semestre 1~5** → destaca o semestre ativo e atualiza o número exibido
- **Disciplinas (pills)** → destaca a disciplina ativa e atualiza o número da matéria
- **Bimestre (accordion)** → abre/fecha a lista de materiais com animação suave
- **Seta ▼ do bimestre** → rotaciona 180° quando aberto

**Linha do tempo de ações:**
```
1. Usuário chega vindo do card na AVA.html
2. Visualiza os semestres disponíveis
3. Clica no semestre desejado (ex: Semestre 2)
4. Visualiza as disciplinas do semestre
5. Clica na disciplina desejada (ex: Tecnologias Móveis)
6. Clica no Bimestre para expandir
7. Acessa o material (Aula, Atividade, Plano de ensino)
```

---

## ⏱ LinhaTempo.html

**Botões e interações:**
- **Filtro "Mostrar tudo"** → filtra grupos exibidos (Importantes / Próximos / Recentes)
- **Ignorar** → remove o item com animação de saída (fade + slide)
- **Auto-remoção do grupo** → se todos os itens forem ignorados, o grupo some também

**Linha do tempo de ações:**
```
1. Usuário acessa via menu "Linha do tempo"
2. (opcional) Usa o filtro para ver só Importantes
3. Lê os itens vencidos destacados em vermelho
4. Clica em "Ignorar" nos itens que não precisa mais ver
5. Verifica próximos eventos e recentes
```

---

## 👤 PerfilUsuario.html

**Botões:**
- **Idioma → Português(Brasil)** → link para configurações de idioma
- **Privacidade → Configurações de visibilidade** → link para configurações de perfil
- **Notificações → Linha do tempo** → navega para `LinhaTempo.html`
- **Notificações → E-mail e Push** → link para configurações de notificação

**Linha do tempo de ações:**
```
1. Usuário clica no avatar/nome no cabeçalho
2. Visualiza foto, nome e informações básicas
3. (opcional) Clica em "Idioma" para alterar idioma
4. (opcional) Clica em "Privacidade" para ajustar visibilidade
5. (opcional) Clica em "Linha do tempo" para ver atividades
```

---

## 🔄 Fluxo Completo entre Telas

```
    Login
      ↓ (Fazer login)
     AVA
      ↓(Card do curso)  → (Linha do tempo)     → (Avatar/Nome)
Sala de Aula              Linha do Tempo         Perfil do Usuário
      ↓                                               ↓                                    ↓
(Materiais/Bimestres)    (Ignorar itens)          (Configurações)
                               ↑_________________________↑
                               (todos voltam ao cabeçalho para navegar)
                                                  ↓
                                      Fazer Logoff (ponto de saída)
                                                  ↓
                                                Login 
```

---

> **Padrão de navegação:** O cabeçalho fixo em todas as telas garante que o usuário sempre consiga acessar qualquer seção sem se perder, seguindo a heurística de Nielsen — **"o usuário sempre sabe onde está e para onde pode ir."**
