# Sistema de Gerenciamento de Biblioteca (Refatorado com SOLID e Clean Code)

## Parte 1: Violações Identificadas

1. SRP: `GerenciadorBiblioteca.AdicionarUsuario` mistura cadastro e notificação.
2. OCP: `GerenciadorBiblioteca.RealizarEmprestimo` depende de lógica fixa de envio de SMS e e-mail.
3. DIP: classe de alto nível depende diretamente de implementações concretas.
4. Clean Code: métodos longos e com múltiplas responsabilidades.
5. LSP: ausência de abstrações impede substituições seguras.

## Parte 2: Refatoração

- Responsabilidades separadas em serviços distintos
- Inversão de dependência via interfaces (`INotificador`)
- Notificações desacopladas da lógica principal
- Métodos curtos, com nomes claros
- Funcionalidade original mantida
