# 📊 Diagnóstico de Code Smells — Sistema de Biblioteca

## Parte 3 — Documentação Consolidada

| # | Code Smell | Localização | Problema | Refatoração | Técnica |
|---|------------|------------|----------|-------------|--------|
| 1 | God Class | SistemaBiblioteca | Classe gerencia múltiplas responsabilidades (livros, usuários, empréstimos, email, relatórios) | Extrair classes de domínio e serviços | Extract Class |
| 2 | Primitive Obsession | livros[][], usuarios[][] | Uso de arrays com índices mágicos (l[0], u[2]) | Criar classes tipadas (Livro, Usuario, Emprestimo) | Replace Data Value with Object |
| 3 | Long Method | realizarEmprestimo() | Método muito grande com várias responsabilidades | Dividir em métodos menores | Extract Method |
| 4 | Switch / Magic Strings | if/else tipo usuário | Uso de strings como "PROFESSOR" e "FUNCIONARIO" | Usar enum + mapa de comportamento | Replace Conditional with Polymorphism |
| 5 | Feature Envy | calcularMulta(), gerarRelatorio() | Métodos usam mais dados de outras classes | Mover métodos para classes corretas | Move Method |
| 6 | Inappropriate Intimacy | enviarEmail() | Lógica de infraestrutura dentro da classe principal | Criar EmailService com injeção de dependência | Extract Class + Dependency Injection |
| 7 | Magic Numbers | 2.50, 14 | Valores fixos sem significado | Criar constantes nomeadas | Replace Magic Number with Constant |
| 8 | Divergent Change | gerarRelatorio() | Método cresce a cada novo tipo | Usar Strategy Pattern | Extract Class + Strategy Pattern |

---

## ALUNOS: jOAO PAULO SASSAKI MAXIMIANO DOS SANTOS | MATHEUS MENEZES | GUILHERME CALDEIRA