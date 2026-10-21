# Política de Privacidade do PontoCerto

**Data de vigência:** 10 de agosto de 2026
**Última atualização:** 21 de outubro de 2026

O PontoCerto é um aplicativo pessoal de controle de ponto e cálculo de horas de trabalho, desenvolvido por Renato Ferraz ("desenvolvedor", "nós"). Esta Política de Privacidade explica quais dados o app trata, onde ficam armazenados e como você pode controlá-los.

Ao usar o PontoCerto, você concorda com as práticas descritas aqui. Se não concordar, não utilize o app.

---

## 1. Resumo rápido

- Seus registros de ponto, horários, ciclos, alarmes e o seu perfil ficam **no seu dispositivo** e, se o iCloud estiver ativo, são sincronizados **pela sua própria conta iCloud** (CloudKit, container privado `iCloud.br.com.renatoferraz.pontocerto`). O desenvolvedor **não tem acesso** a esses dados.
- O app inclui o **UAPPKit**, um componente do próprio desenvolvedor que mostra as telas Sobre, Novidades, Roadmap e Feedback. Só quando você **envia uma sugestão, um comentário ou um voto**, ou **entra numa conta UAPP** (opcional), alguns dados seus vão para os servidores do UAPP (seção 4).
- As assinaturas do PontoCerto Pro são vendidas e cobradas pela **Apple**. Não recebemos seus dados de pagamento.
- **Não usamos** analytics, rastreamento entre apps, anúncios ou identificador de publicidade.
- **Não vendemos nem alugamos** seus dados.

---

## 2. Dados tratados pelo app

### Dados que ficam só nos seus dispositivos e no seu iCloud

- Horários de entrada, intervalo e saída, registrados por você ou confirmados a partir de um alarme ou lembrete.
- Configuração de jornada, ciclo mensal, feriados, pausas, alarmes e notificações.
- Perfil local: nome, e-mail e foto que você escolher preencher em Ajustes › Perfil.
- Arquivos de backup, gravados no próprio dispositivo ou onde você decidir exportá-los.

### Dados enviados ao UAPP (somente quando você usa esses recursos)

- **Ao enviar uma sugestão, um comentário ou um voto** no Feedback ou no Roadmap: o texto, as imagens que você anexar e a sua identificação de autor (nome, e-mail e foto do seu perfil local ou da conta UAPP), para que a sugestão apareça com o seu nome e você possa receber resposta.
- **Ao entrar numa conta UAPP** (opcional; por e-mail ou pelos provedores de login oferecidos na tela): nome, e-mail, foto de perfil e o identificador da conta.
- **Ao abrir as telas do UAPPKit** (Sobre, Novidades, Roadmap, Avaliações): o app pede essas informações ao servidor do UAPP informando qual é o app e o idioma. Como em qualquer acesso à internet, o servidor recebe o endereço IP da conexão.

### Dados tratados pela Apple

- **Compras e assinaturas:** feitas pela App Store. A Apple processa o pagamento; o app recebe só a confirmação de que a assinatura está ativa.
- **Alarmes e notificações:** o app usa o AlarmKit e as notificações do sistema; o agendamento fica no próprio sistema operacional.
- **Câmera e fotos:** usadas apenas quando você escolhe tirar ou selecionar a foto do perfil. Nada é enviado sem a sua ação.

### O que o app NÃO coleta

- Localização, contatos, dados de saúde, histórico de navegação ou identificador de publicidade.
- Registros de ponto, horários, saldo ou histórico: esses dados nunca vão para o UAPP nem para o desenvolvedor.
- Não rastreamos você entre apps ou sites.

---

## 3. Como os dados são armazenados e sincronizados

- **Armazenamento local:** Core Data, no armazenamento protegido do iOS, iPadOS, macOS e watchOS.
- **Sincronização:** CloudKit, no **container privado** da sua conta iCloud. Os dados sincronizados só existem dentro do espaço do seu Apple ID, o mesmo mecanismo usado por apps como Lembretes ou Notas.
- **Widgets e Apple Watch:** leem os mesmos dados por um App Group local (`group.br.com.renatoferraz.pontocerto`), pelo CloudKit privado e pela conexão direta entre o iPhone e o relógio.
- O desenvolvedor não opera, não acessa e não tem meio técnico de acessar o conteúdo do seu container CloudKit privado.

---

## 4. UAPP e compartilhamento de dados

O UAPP é a plataforma do próprio desenvolvedor para receber sugestões, publicar novidades e manter o roadmap dos apps. Os dados enviados a ele (seção 2) ficam nos servidores do UAPP, hospedados pela Supabase, e são usados apenas para:

- mostrar sua sugestão ou comentário no Roadmap do PontoCerto, com o seu nome e foto como autor;
- responder você e avisar sobre o andamento da sua sugestão;
- manter sua conta UAPP, se você criar uma.

Sugestões, comentários e votos publicados no Roadmap podem ser vistos por outras pessoas que usam o app, junto com o nome e a foto do autor. Não envie dados sensíveis nesses textos.

O tratamento dos dados da conta UAPP também segue a [Política de Privacidade do UAPP](https://uapp.renatoferraz.net/politica-de-privacidade).

Fora isso, não compartilhamos dados com terceiros. A Apple participa do armazenamento (iCloud/CloudKit) e das compras (App Store), regidos pela [Política de Privacidade da Apple](https://www.apple.com/legal/privacy/br/). Podemos divulgar informações se exigido por lei ou ordem judicial válida.

---

## 5. Segurança

- Os dados no dispositivo seguem a criptografia padrão do iOS, macOS e watchOS.
- Os dados sincronizados pelo CloudKit seguem a criptografia em trânsito e em repouso da Apple.
- A comunicação com o UAPP usa conexão criptografada (HTTPS).
- Nenhum método de armazenamento é 100% seguro. Proteja sua conta Apple com senha forte e autenticação de dois fatores.

---

## 6. Seus direitos e controle (LGPD)

- **Acesso e correção:** seus registros e o seu perfil ficam visíveis e editáveis no próprio app, a qualquer momento.
- **Exportação:** o backup em arquivo (Ajustes › Backup) gera uma cópia dos seus dados que você pode guardar ou levar para outro aparelho.
- **Exclusão dos dados do app:** apagar os registros dentro do app ou desinstalá-lo remove os dados do dispositivo; desligar o iCloud para o app (Ajustes › [seu nome] › iCloud) e apagar os dados dele remove o que está no CloudKit.
- **Exclusão dos dados do UAPP:** você pode sair da conta UAPP em Ajustes. Para excluir a conta UAPP, as sugestões e os comentários enviados, escreva para o e-mail abaixo; o pedido é atendido no prazo previsto pela LGPD.
- **Revogar permissões:** câmera, fotos, notificações e alarmes podem ser desligados a qualquer momento nos Ajustes do sistema.

Em caso de dúvidas sobre tratamento de dados pessoais nos termos da Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018), entre em contato pelo e-mail abaixo.

---

## 7. Crianças

O PontoCerto não é direcionado a crianças. É um app de controle de jornada de trabalho, destinado a usuários maiores de 18 anos ou em idade legal de trabalho.

---

## 8. Alterações nesta política

Podemos atualizar esta Política de Privacidade quando o app ganhar recursos que mudem o tratamento de dados. A data de "Última atualização" no topo será revisada, e alterações relevantes serão comunicadas dentro do próprio app.

---

## 9. Contato

Dúvidas sobre esta Política de Privacidade:

- **E-mail:** renatodesenv@icloud.com
- **Desenvolvedor:** Renato Ferraz
