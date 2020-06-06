# Recuperação de senha

**RF (Requisitos Funcionais)**

- O usuário deve poder recuperar sua senha informando o seu email;
- O usuário deve receber um e-mail com instruções de recuperação de senha;
- O usuário deve poder resetar sua senha;

**RNF (Requisitos não funcionais)**

- Utilizar Mailtrap para testar envios em ambiente de dev;
- Utilizar o Amazon SES para envios em produção;
- O envio de e-mails deve acontecer em segundo plano (background job);

**RN (Regras de Negócios)**

- O link enviado por email para resgatar senha, deve expirar em 2h;
- O usuário precisa confirmar a nova senha ao resetar a sua senha;

# Atualização do Perfil

**RF (Requisitos Funcionais)**

- O usuário deve poder atualizar o seu nome, email e senha;

**RN (Regras de Negócios)**
- O usuário não pode alterar seu email para um email já utilizado;
- Para atualizar a sua senha, o usuário deve informar a senha antiga;
- Para atualizar a sua senha, o usuário precisa confirmar a nova senha;

# Painel do Prestador

**RF (Requisitos Funcionais)**

- O usuário deve poder listar todos os seus agendamentos de um dia específico;
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas;

**RNF (Requisitos não funcionais)**

- Os agendamentos do dia

**RN (Regras de Negócios)**
- A notificação deve ter um status de lida ou não-lida para que o prestador possa controlar;

# Agendamento de Serviços

**RF (Requisitos Funcionais)**

- O usuário deve poder listar todos os prestadores de serviço cadastrados;
- O usuário deve postar os dias de um mês com pelo menos um horário disponível de um prestador;
- O usuário deve poder listar os horários dispóniveis em um dia especifico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;

**RNF (Requisitos não funcionais)**

- A listagem de prestadores deve ser armazenado em cache;
- As notificações do prestador devem ser armazenados em MongoDB;
- As notificações do prestador devem ser enviadas em tempo-real utilizando Socket.io;

**RN (Regras de Negócios)**

- Cada agendamento deve durar 1h exatamente;
- Os agendamentos devem estar disponíveis entre 8h às 18hr (Primeiro às 8h, último às 17h);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar serviços consigo mesmo;

