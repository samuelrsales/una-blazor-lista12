# EcoMonitor - Lista 12 (Blazor) 🌱

> Transformando pequenas ações em grande impacto ambiental com Blazor Interactive Server.

---

## 👤 Identificação

| Campo         | Informação                            |
| ------------- | ------------------------------------- |
| Nome completo | Samuel Rodrigues Sales                |
| Curso         | Análise e Desenvolvimento de Sistemas |
| Disciplina    | Interação Humano Computador e UX      |
| Professor     | Daniel Henrique Matos de Paiva        |
| Instituição   | Centro Universitário UNA              |

## 📌 Sobre o Projeto

O **EcoMonitor** é uma prova de conceito de gamificação para a ONG **ReCiclo**.
Nesta aplicação, o usuário registra ações sustentáveis e acompanha a pontuação acumulada em tempo real.

Cada ação é representada por um card reutilizável com:

- parâmetro de peso da ação;
- estado dinâmico de pontuação;
- feedback visual de progresso e conquista.

## 🧠 Heurísticas de Nielsen Aplicadas

### 1. Visibilidade do status do sistema

Após cada clique no botão **Registrar Atividade**, o total acumulado é atualizado imediatamente, mostrando ao usuário o estado atual do sistema.

### 2. Feedback imediato

A interface responde instantaneamente à interação com atualização de contador, avanço da barra de progresso e mensagem de conquista ao atingir a meta.

### 3. Consistência e padrões

Os três cards seguem o mesmo padrão visual e funcional, mudando apenas os parâmetros (título, peso e meta), o que reduz carga cognitiva e facilita o uso.

## ⚙️ Guia de Execução (Terminal)

### Pré-requisitos

- .NET SDK instalado

### Passos

1. Restaurar dependências:

```bash
dotnet restore
```

2. Executar o projeto com perfil HTTPS:

```bash
dotnet run --launch-profile https
```

3. Abrir no navegador o endereço informado no terminal:

```text
https://localhost:PORTA
```

## 🧩 Explicação Técnica sobre [Parameter]

O componente `EcoStatus` foi criado para ser reutilizável com parâmetros públicos:

- `Titulo`: define o nome da ação sustentável.
- `PesoAcao`: define quantos pontos são adicionados por clique.
- `Meta`: define o objetivo para destaque visual e mensagem de conquista.

Na página inicial, o mesmo componente é usado três vezes com valores diferentes. Isso permite reaproveitar estrutura e lógica sem duplicação de código.

Cada instância mantém seu próprio estado interno (`TotalAcumulado`), garantindo independência entre os cards.

## ✅ Funcionalidades Implementadas

- [x] Componente reutilizável com parâmetros personalizáveis
- [x] Estado dinâmico por card
- [x] Incremento por clique com base no peso da ação
- [x] Estilização condicional ao atingir meta
- [x] Barra de progresso
- [x] Mensagem de conquista ao atingir a meta

---

## 🚀 Resultado Esperado

O usuário consegue registrar ações sustentáveis em diferentes categorias e visualizar, em tempo real, sua evolução e impacto ambiental.
