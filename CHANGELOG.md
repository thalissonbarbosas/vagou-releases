# Changelog

Todas as mudanças relevantes do Vagou ficam registradas aqui.

O formato segue o [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/),
e o projeto segue o [Versionamento Semântico](https://semver.org/lang/pt-BR/).

## [0.6.0] - 2026-10-10

### Adicionado
- Conexões mostra dois quadros, Planos de saúde e Ingressos. Cada um abre sua própria lista: cada plano disponível com as contas conectadas e um botão "Conectar uma conta", e a Ticketmaster com os eventos monitorados.
- "Monitorar" abre os mesmos quadros para você escolher o que vigiar, e a tela inicial vazia começa do mesmo jeito. Sem plano conectado, Planos de saúde leva primeiro a conectar um.
- Monitoramentos de ingressos e a conexão da Ticketmaster mostram o logo da Ticketmaster.

### Alterado
- Uma conta que precisa de atenção mostra um aviso no quadro Planos de saúde, e a notificação dela abre direto a lista de planos.
- O plano de demonstração com dados fictícios foi removido.

### Corrigido
- Os monitoramentos de ingressos voltaram a funcionar. A Ticketmaster desativou o endereço de onde o Vagou lia os eventos, e toda verificação falhava com "A Ticketmaster pediu uma pausa".
- Quando a Ticketmaster bloqueia a conexão (comum em VPNs), o monitoramento diz "A Ticketmaster bloqueou a consulta" em vez de pedir uma pausa.

## [0.6.0] - 2026-10-10

### Added
- Conexões shows two boxes, Planos de saúde and Ingressos. Each opens its own list: every available plan with its connected accounts and a "Conectar uma conta" button, and Ticketmaster with its watched events.
- "Monitorar" opens the same boxes so you pick what to watch, and an empty Home starts the same way. Without a connected plan, Planos de saúde takes you to connect one first.
- Ticket watches and Ticketmaster connections show the Ticketmaster logo.

### Changed
- An account that needs attention shows a badge on the Planos de saúde box, and its notification opens the plan list directly.
- The demonstration plan with fictitious data is gone.

### Fixed
- Ticket watches work again. Ticketmaster shut the address Vagou read events from, so every check failed with "A Ticketmaster pediu uma pausa".
- When Ticketmaster blocks the connection (common on VPNs), the watch says "A Ticketmaster bloqueou a consulta" instead of asking for a pause.

## [0.5.0] - 2026-10-07

### Adicionado
- Monitoramento de ingressos da Ticketmaster Brasil, sem conta: cole o link do evento ou compartilhe com o Vagou, escolha datas, setores e tipos de ingresso (Inteira, Meia-entrada, PCD, Idoso), e o Vagou toca um alarme, repetindo até você ver, quando um ingresso que serve fica disponível ou quando a venda abre. Tocar no aviso abre a página de venda do evento.
- Páginas de evento que reúnem várias cidades ou datas deixam você escolher qual venda monitorar.
- Os monitoramentos de ingressos verificam de 15 segundos a 5 minutos enquanto a notificação fixa "Vagou está de olho nos ingressos" aparece; o botão "Pausar" dela interrompe.

### Alterado
- A aba Contas agora se chama Conexões e lista seus planos de saúde e a Ticketmaster.
- Os Termos de Uso e a Política de Privacidade agora cobrem o monitoramento de ingressos, por isso você vai aceitá-los de novo.

## [0.4.0] - 2026-09-25

### Alterado
- As vagas encontradas agora vêm com um lembrete para confirmar os horários no app da Humana antes de agendar.

## [0.3.0] - 2026-09-24

### Adicionado
- "Todas as unidades": um monitoramento por nome de médico agora pode buscar em todas as unidades da especialidade, como a busca por nome do app oficial, em vez de só nas unidades escolhidas. O editor mostra onde atende o médico encontrado.
- Um monitoramento pode combinar médicos escolhidos com um nome de médico: você recebe vagas dos médicos escolhidos e de qualquer um cujo nome combine.

### Alterado
- Mudar as unidades de um monitoramento mantém o nome de médico digitado e os médicos escolhidos que ainda atendem lá.

### Corrigido
- Monitoramentos por nome de médico ou por qualquer médico agora enxergam um médico que acabou de abrir agenda online na próxima verificação, em vez de até 24 horas depois.

## [0.2.0] - 2026-09-24

### Adicionado
- Uma notificação fixa e silenciosa mostra quantos monitoramentos estão rodando e quando é a próxima verificação. O botão "Desativar" dela a desliga até você reativar em Ajustes > Notificação fixa.

### Corrigido
- Especialidades como Cardiologia não falham mais ao listar médicos quando algumas unidades não têm médico com agenda online; essas unidades só aparecem vazias.
- Quando a lista de médicos de uma unidade não carrega, as outras unidades continuam aparecendo, e você ainda pode monitorar qualquer médico pelo nome.
- Uma verificação em várias unidades não falha mais por inteiro quando uma unidade responde num formato inesperado; essa unidade é pulada e as outras são verificadas.

## [0.1.0] - 2026-09-24

Primeira versão do piloto. O Vagou vigia a agenda do seu plano de saúde pelo celular e avisa quando abre uma vaga com o médico que você quer. Tudo fica no celular: sem servidor, sem cadastro, sem telemetria.

### Adicionado
- Suporte à Humana Saúde Nordeste: conecte com o login do portal do beneficiário, veja os planos e pacientes (titular e dependentes) da conta, e escolha especialidades, unidades e médicos nas listas do próprio portal.
- Monitoramentos: escolha o plano, o paciente, a especialidade e uma ou mais unidades, e então qualquer médico, médicos específicos ou qualquer médico cujo nome contenha o que você digitar. Limite por datas, dias da semana e horário, e defina a frequência: a cada 10 minutos no mínimo, com um mínimo maior para monitoramentos que cobrem muitos médicos.
- Verificações em segundo plano que continuam com o app fechado, e uma notificação assim que surge uma vaga nova, com atalho para o app oficial do plano para agendar.
- Avisos quando uma conta precisa de você (senha errada, conta bloqueada, novos termos para aceitar no portal): as verificações dela pausam até você retomar, e o Vagou nunca aceita nada por você.
- Avisos quando o portal do plano está fora do ar ou as verificações estão atrasadas.
- Detalhes do monitoramento com as vagas encontradas, agrupadas por dia e por médico, cada médico com sua cor, e filtro por médico. Vagas ocupadas ou passadas saem da lista.
- Histórico de atividade do que foi verificado e encontrado.
- Tela de contas com as carteirinhas dos seus planos.
- Plano de demonstração ("Demonstração") com dados fictícios, para experimentar todas as telas sem login de plano.
- Ajustes: tema claro por padrão (escuro ou seguir o sistema), notificações discretas que só dizem "Nova vaga encontrada", detalhes na tela de bloqueio ligados ou desligados, pausar tudo, relatório de diagnóstico sem dados pessoais, e "Apagar tudo" para apagar tudo o que o Vagou guardou no celular.
- Termos de Uso e Política de Privacidade para aceitar na primeira abertura, que podem ser lidos a qualquer momento em Ajustes.

### Corrigido
- O login da Humana não para mais na etapa do plano, bloqueado pela proteção Cloudflare do portal.
- Os links para a Política de Privacidade dentro dos Termos de Uso agora abrem a política.
- Em contas com mais de um plano, as verificações de um plano agora rodam na sessão do portal desse plano. Antes, podiam rodar no último plano selecionado e não achar nada, ou achar as vagas erradas.
- Uma vaga que some numa verificação e volta não aparece mais como ocupada, e editar o que um monitoramento busca recomeça os resultados em vez de marcar os antigos como ocupados.
- "Verificar agora" diz quando a próxima verificação manual libera em vez de não fazer nada.

### Segurança
- Senhas, sessões e todos os dados do app são criptografados com uma chave guardada no Android Keystore, e ficam fora dos backups e das transferências entre aparelhos.
- O Vagou só conversa com os endereços do próprio portal do plano, por HTTPS, confiando apenas nos certificados do sistema. Sem analytics, relatório de falhas ou anúncios.
- A tela de login não aparece em capturas de tela nem na prévia de apps recentes.

