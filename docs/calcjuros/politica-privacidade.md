# Política de Privacidade do CalcJuros

**Data de vigência:** 27 de outubro de 2026
**Última atualização:** 27 de outubro de 2026

O CalcJuros é uma calculadora financeira para iPhone, iPad e Apple Watch, desenvolvida por Renato Ferraz ("desenvolvedor", "nós"). Esta Política de Privacidade explica quais dados o app trata, onde ficam armazenados e como você pode controlá-los.

Ao usar o CalcJuros, você concorda com as práticas descritas aqui. Se não concordar, não utilize o app.

---

## 1. Resumo rápido

- O app **não exige conta**. Seus cálculos, clientes, cheques, empréstimos e o seu perfil ficam **no seu dispositivo** e são sincronizados **pela sua própria conta iCloud** (CloudKit, container privado `iCloud.br.renatoferrazdf.calcjuros`). O desenvolvedor **não tem acesso** a esses dados.
- O login com uma conta antiga (Firebase, do Google) existe **só para importar** os dados de versões anteriores do app.
- O app inclui o **UAPPKit**, componente do próprio desenvolvedor que mostra Sobre, Novidades, Roadmap e Feedback. Alguns dados do seu perfil vão para o UAPP para identificar você nesses recursos (seção 4).
- As assinaturas são vendidas e cobradas pela **Apple**. Não recebemos seus dados de pagamento.
- **Não vendemos nem alugamos** seus dados, não exibimos anúncios e não rastreamos você entre apps de outras empresas.

---

## 2. Dados tratados pelo app

### Dados que ficam só nos seus dispositivos e no seu iCloud

- **Cálculos** que você salva, com os valores informados e os resultados.
- **Perfil:** nome, foto, e-mail e celular que você escolher preencher.
- **Clientes, cheques e empréstimos** que você cadastrar, que podem incluir nome, endereço, telefone, CPF, observações, valores, datas e parcelas de outras pessoas.
- **Preferências:** favoritas, idioma, horários de aviso e configuração do bloqueio do app.
- **Backups** criptografados, gravados no próprio dispositivo ou onde você decidir exportá-los.

### Dados enviados ao UAPP

- **Ao abrir o app com um perfil:** o identificador do perfil, o e-mail e o nome, para que as sugestões, os votos e as respostas no Feedback e no Roadmap fiquem associados a você.
- **Ao enviar uma sugestão, um comentário ou um voto:** o texto, as imagens que você anexar e a sua identificação de autor (nome, e-mail, celular e foto do perfil).
- **Ao abrir as telas do UAPPKit:** o app pede as informações ao servidor do UAPP informando qual é o app e o idioma. Como em qualquer acesso à internet, o servidor recebe o endereço IP da conexão.

### Dados tratados pelo Google (Firebase), só para quem importa dados antigos

- **Ao entrar com a conta antiga** (e-mail e senha, Google ou Apple): o Firebase Authentication confirma a conta, e o app lê no Firestore os cálculos, clientes, cheques e operadoras dessa conta para copiá-los para o seu iCloud. O app registra no servidor antigo que a importação foi feita.
- **Firebase Analytics:** o app inclui o SDK do Firebase Analytics, que registra eventos técnicos (por exemplo, a conclusão da importação) e pode coletar um identificador de instância do app, dados do dispositivo e de uso, de forma agregada. Esses dados não são usados para publicidade.

### Outros serviços consultados pelo app

- **Banco Central do Brasil:** a correção monetária e o rendimento comparado buscam séries públicas de índices (IPCA, INPC, IGP-M, Selic, CDI) na API do Banco Central. Nenhum dado pessoal é enviado.
- **Tabelas de salário:** as tabelas de INSS e Imposto de Renda são lidas de um banco de dados do desenvolvedor, hospedado pela Supabase. Nenhum dado pessoal é enviado.
- **Verificação de conexão:** para saber se há internet, o app faz pedidos simples a endereços públicos do Google. Nenhum dado pessoal é enviado.

Nesses acessos, como em qualquer acesso à internet, os servidores recebem o endereço IP da conexão.

### Dados tratados pela Apple

- **Compras e assinaturas:** feitas pela App Store. A Apple processa o pagamento; o app recebe só a confirmação da assinatura e o recibo de compra, usado também para reconhecer quem comprou uma versão anterior.
- **Notificações:** os avisos de vencimento são agendados no próprio aparelho.
- **Face ID e Touch ID:** a verificação é feita pelo sistema; o app recebe só se ela deu certo. O PIN do bloqueio fica no próprio aparelho.
- **Câmera e fotos:** usadas apenas quando você lê o código de barras de um boleto ou escolhe a foto do perfil. As imagens do boleto não são guardadas.

### O que o app NÃO coleta

- Localização, contatos da agenda, dados de saúde, histórico de navegação ou identificador de publicidade.
- Seus cálculos, clientes, cheques e empréstimos nunca vão para o UAPP nem para o desenvolvedor.

---

## 3. Como os dados são armazenados e sincronizados

- **Armazenamento local:** Core Data, no armazenamento protegido do iOS, iPadOS e watchOS.
- **Sincronização:** CloudKit, no **container privado** da sua conta iCloud, o mesmo mecanismo usado por apps como Lembretes e Notas. Algumas preferências usam o armazenamento de chaves do iCloud.
- **Widgets e Apple Watch:** leem os mesmos dados por um grupo de apps local e pela conexão entre o iPhone e o relógio.
- O desenvolvedor não opera, não acessa e não tem meio técnico de acessar o conteúdo do seu container CloudKit privado.

---

## 4. Compartilhamento de dados

O UAPP é a plataforma do próprio desenvolvedor para receber sugestões, publicar novidades e manter o roadmap dos apps. Os dados enviados a ele ficam nos servidores do UAPP, hospedados pela Supabase, e são usados apenas para:

- mostrar sua sugestão ou comentário no Roadmap do CalcJuros, com o seu nome e foto como autor;
- responder você e avisar sobre o andamento da sua sugestão.

Sugestões, comentários e votos publicados no Roadmap podem ser vistos por outras pessoas que usam o app, junto com o nome e a foto do autor. Não envie dados sensíveis nesses textos. O tratamento desses dados também segue a [Política de Privacidade do UAPP](https://uapp.renatoferraz.net/politica-de-privacidade).

O Google (Firebase) trata os dados descritos na seção 2 conforme a [Política de Privacidade do Google](https://policies.google.com/privacy). A Apple participa do armazenamento (iCloud) e das compras (App Store), regidos pela [Política de Privacidade da Apple](https://www.apple.com/legal/privacy/br/).

Fora isso, não compartilhamos dados com terceiros. Podemos divulgar informações se exigido por lei ou ordem judicial válida.

---

## 5. Dados de terceiros que você cadastra

Os dados de clientes que você cadastra (como nome, telefone, endereço e CPF) ficam só no seu aparelho e no seu iCloud. Em relação a eles, **você é o controlador** nos termos da LGPD: decide o que cadastrar, para que usar e quando apagar. O desenvolvedor não acessa nem usa esses dados. Ao enviar uma cobrança pelo WhatsApp ou por mensagem, o conteúdo sai do seu aparelho pelo app que você escolher.

---

## 6. Segurança

- Os dados no dispositivo seguem a criptografia padrão do iOS, iPadOS e watchOS, e o app pode ser bloqueado por PIN, Face ID ou Touch ID.
- Os backups gerados pelo app são criptografados.
- Os dados sincronizados pelo CloudKit seguem a criptografia em trânsito e em repouso da Apple.
- A comunicação com o UAPP, o Firebase e as demais APIs usa conexão criptografada (HTTPS).
- Nenhum método de armazenamento é 100% seguro. Proteja sua conta Apple com senha forte e autenticação de dois fatores.

---

## 7. Seus direitos e controle (LGPD)

- **Acesso e correção:** seus cálculos, clientes e o seu perfil ficam visíveis e editáveis no próprio app.
- **Exportação:** o backup em arquivo gera uma cópia dos seus dados que você pode guardar ou levar para outro aparelho.
- **Exclusão dos dados do app:** em Ajustes, a exclusão do perfil apaga o perfil, os clientes, os cheques e os cálculos deste aparelho e do seu iCloud. Apagar itens dentro do app ou desinstalá-lo também remove dados do aparelho.
- **Exclusão dos dados do UAPP e da conta antiga:** para apagar sugestões e comentários enviados, ou os dados da sua conta antiga no Firebase, escreva para o e-mail abaixo. O pedido é atendido no prazo previsto pela LGPD.
- **Revogar permissões:** câmera, fotos, notificações e Face ID podem ser desligados a qualquer momento nos Ajustes do sistema.

Em caso de dúvidas sobre tratamento de dados pessoais nos termos da Lei Geral de Proteção de Dados (LGPD, Lei nº 13.709/2018), entre em contato pelo e-mail abaixo.

---

## 8. Crianças

O CalcJuros não é direcionado a crianças. É um app de cálculos financeiros e controle de carteira, destinado a maiores de 18 anos.

---

## 9. Alterações nesta política

Podemos atualizar esta Política de Privacidade quando o app ganhar recursos que mudem o tratamento de dados. A data de "Última atualização" no topo será revisada, e alterações relevantes serão comunicadas dentro do próprio app.

---

## 10. Contato

Dúvidas sobre esta Política de Privacidade:

- **E-mail:** renatodesenv@icloud.com
- **Desenvolvedor:** Renato Ferraz

[English version](en/privacy-policy.md)
