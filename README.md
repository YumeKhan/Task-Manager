# 📝 Task Manager React

Um gerenciador de tarefas moderno e intuitivo construído com **React.js**. Este projeto foi desenvolvido para organizar o fluxo de trabalho diário, permitindo a transição de tarefas entre diferentes estados de conclusão.

## 🚀 Funcionalidades
* **Adicionar Tarefas:** Criação dinâmica com geração de ID único.
* **Gerenciamento de Estados:** Organização automática entre as colunas "Pendente", "Fazendo" e "Completa".
* **Edição em tempo real:** Atualização de títulos e estados das tarefas existentes.
* **Exclusão:** Remoção de tarefas com atualização imediata da interface.
* **Componentização:** Estrutura limpa dividida em Navbar e TaskLists.

## 🛠️ Tecnologias Utilizadas
* **React.js** (Hooks: `useState`)
* **JavaScript (ES6+)**
* **CSS3** (Estilização customizada)
* **HTML5**

## 🎨 Preview do Projeto
![Task Manager Preview]<img width="1238" height="712" alt="image" src="https://github.com/user-attachments/assets/bd5acf94-2618-4df1-83e7-62e076c2970f" />

## 🏗️ Estrutura do Código
O coração da aplicação utiliza o hook `useState` para gerenciar um array de objetos, garantindo a imutabilidade dos dados durante as operações de filtro e mapeamento:

```javascript
// Exemplo da lógica de atualização de tarefas
const updateTask = (id, title, state) => {
  setTasks((existingTasks) => {
    return existingTasks.map((task) => {
      if (task.id === id) {
        return { ...task, title, state };
      }
      return task;
    });
  });
};

