---
title: Política de Privacidade do MediCasa
lang: pt
---

# Política de Privacidade do MediCasa

**Data de vigência:** 5 de novembro de 2026
**Última atualização:** 5 de novembro de 2026

O MediCasa é um aplicativo de organização de remédios em casa (lembretes de dose, estoque, compras, vencimentos e casa compartilhada com a família), desenvolvido por Renato Ferraz ("desenvolvedor", "nós"). Esta Política de Privacidade explica quais dados o app trata, onde ficam e como você pode controlá-los.

Ao usar o MediCasa, você concorda com as práticas descritas aqui. Se não concordar, não utilize o app.

---

## 1. Resumo rápido

- O MediCasa precisa de uma **conta** (e-mail e senha, Iniciar sessão com a Apple ou Google). Seus remédios, lembretes, doses, compras e farmácias ficam na sua conta, nos servidores do **Firebase** (Google), para sincronizar entre os seus aparelhos e com as pessoas da sua casa.
- A **leitura da foto da caixa** e a **descrição "Para que serve"** são feitas **no próprio aparelho**, pelo Vision e pelo Apple Intelligence. As fotos da caixa não são enviadas para nenhum servidor.
- As assinaturas do Premium são vendidas e cobradas pela **Apple**. Não recebemos seus dados de pagamento.
- **Não usamos** analytics, rastreamento entre apps, anúncios ou identificador de publicidade.
- **Não vendemos nem alugamos** seus dados.

---

## 2. Dados tratados pelo app

### Dados da conta

- Nome, e-mail, telefone e, se você quiser, apelido, gênero, data de nascimento e foto de perfil.
- Identificador da conta e o provedor de login usado (e-mail, Apple ou Google).
- Idioma e preferências do app (aparência, notificações, alarmes, estoque mínimo e padrões de cadastro).

### Dados que você cadastra

- **Remédios:** nome, composto ativo, tipo, unidade, estoque, lote, fabricação, validade, código de barras e o texto "Para que serve".
- **Lembretes e doses:** horários, repetição, observações e o registro das doses tomadas, puladas ou adiadas, inclusive de remédios de pets (com o nome do pet, se você informar).
- **Compras e farmácias:** data, farmácia, quantidades, preços, descontos e os dados da farmácia (nome, telefone e endereço).
- **Casa compartilhada:** nome da casa e as pessoas que fazem parte dela. Os remédios, lembretes e compras da casa ficam visíveis para todos os membros.

Esses dados podem revelar informações sobre a sua saúde e a da sua família. Eles são usados **somente para o funcionamento do app** e nunca para publicidade.

### Dados técnicos

- Tokens de notificação (APNs e Firebase Cloud Messaging), para entregar avisos e sincronizar alarmes entre aparelhos.
- Verificação de integridade do app (Firebase App Check), que confirma que as chamadas vêm do MediCasa original.
- Como em qualquer acesso à internet, os servidores recebem o endereço IP da conexão.

### Dados tratados só no seu aparelho

- **Câmera e fotos:** usadas quando você fotografa a caixa, o lote ou o código de barras, ou escolhe a foto de perfil. As fotos da caixa são lidas no aparelho e descartadas; só a foto de perfil é enviada (Firebase Storage), para aparecer nos seus aparelhos e para a sua casa.
- **Apple Intelligence:** a descrição "Para que serve" e a tradução das notícias são geradas no aparelho, pelo modelo da Apple.
- **Localização:** usada só quando você busca farmácias próximas, pela busca de mapas da Apple (MapKit). O MediCasa não guarda a sua localização.
- **Alarmes e notificações:** agendados no próprio sistema (AlarmKit e notificações do iOS).

### Dados enviados ao UAPP

O app inclui o **UAPPKit**, um componente do próprio desenvolvedor que mostra as telas Sobre, Novidades e Feedback. Para que suas sugestões apareçam com o seu nome e você possa receber resposta, o app informa ao UAPP o identificador da conta, o nome, o e-mail e a foto de perfil. O texto e as imagens que você enviar no Feedback também vão para o UAPP.

### O que o app NÃO coleta

- Contatos, histórico de navegação, dados do app Saúde ou identificador de publicidade.
- Não rastreamos você entre apps ou sites.

---

## 3. Onde os dados ficam

- **Firebase (Google):** Authentication (login), Cloud Firestore (dados do app), Storage (foto de perfil), Cloud Functions (operações da casa, notificações e notícias) e Cloud Messaging (avisos). O acesso é protegido por regras: cada pessoa lê e grava só os próprios dados e os da casa de que participa.
- **Cache no aparelho:** o app guarda uma cópia dos dados para abrir rápido e funcionar sem internet.
- **Apple Watch e widgets:** recebem os dados do iPhone pela conexão direta entre os aparelhos e por um App Group local.
- **UAPP:** servidores do desenvolvedor, hospedados pela Supabase (seção 2).

---

## 4. Compartilhamento

- **Com a sua casa:** tudo o que é da casa fica visível para os membros dela. Ao sair da casa, você deixa de ver os dados dela; o que é seu continua no seu escopo pessoal.
- **Com prestadores:** Google (Firebase) e Supabase (UAPP) tratam os dados em nosso nome, só para operar o app. A Apple processa as compras pela App Store.
- Fora isso, não compartilhamos dados com terceiros. Podemos divulgar informações se exigido por lei ou ordem judicial válida.

Políticas dos prestadores: [Google/Firebase](https://firebase.google.com/support/privacy), [Apple](https://www.apple.com/legal/privacy/br/) e [UAPP](https://uapp.renatoferraz.net/politica-de-privacidade).

---

## 5. Segurança

- A comunicação com os servidores usa conexão criptografada (HTTPS).
- O Firebase guarda os dados com criptografia em repouso.
- Nenhum método de armazenamento é 100% seguro. Use uma senha forte e não compartilhe o acesso à sua conta.

---

## 6. Seus direitos e controle (LGPD)

- **Acesso e correção:** seus dados ficam visíveis e editáveis no próprio app (Perfil, Remédios, Agenda, Compras e Farmácias).
- **Exclusão da conta:** em Perfil, toque em **Excluir conta**. A conta, a foto de perfil e os seus dados pessoais são apagados. Dados que pertencem a uma casa compartilhada continuam com os outros membros dela.
- **Sair da casa:** em Ajustes › Casa, a qualquer momento.
- **Revogar permissões:** câmera, fotos, localização, notificações e alarmes podem ser desligados nos Ajustes do sistema.
- **Dados do UAPP:** para apagar sugestões enviadas pelo Feedback, escreva para o e-mail abaixo.

Pedidos sobre dados pessoais, nos termos da Lei Geral de Proteção de Dados (LGPD, Lei nº 13.709/2018), são atendidos pelo e-mail abaixo, no prazo previsto em lei.

---

## 7. Crianças

O MediCasa não é direcionado a crianças. A conta deve ser criada por um adulto, que pode cadastrar os remédios de crianças e pets da casa.

---

## 8. Alterações nesta política

Podemos atualizar esta Política de Privacidade quando o app ganhar recursos que mudem o tratamento de dados. A data de "Última atualização" no topo será revisada, e alterações relevantes serão comunicadas dentro do app.

---

## 9. Contato

- **E-mail:** [renatodesenv@icloud.com](mailto:renatodesenv@icloud.com)
- **Desenvolvedor:** Renato Ferraz

[English version](en/privacy-policy.md)
