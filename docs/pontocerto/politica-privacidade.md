# Política de Privacidade do PontoCerto

**Data de vigência:** 10 de agosto de 2026
**Última atualização:** 10 de agosto de 2026

O PontoCerto é um aplicativo pessoal de controle de ponto e cálculo de horas de trabalho, desenvolvido por Renato Ferraz ("desenvolvedor", "nós"). Esta Política de Privacidade explica quais dados o app trata, onde ficam armazenados e como você pode controlá-los.

Ao usar o PontoCerto, você concorda com as práticas descritas aqui. Se não concordar, não utilize o app.

---

## 1. Resumo rápido

- O PontoCerto **não tem servidor próprio**. Não existe backend do desenvolvedor recebendo, processando ou armazenando seus dados.
- Seus registros de ponto, horários, ciclos e alarmes ficam **no seu dispositivo** (Core Data) e, se você tiver o iCloud ativo, são sincronizados **exclusivamente através da sua própria conta iCloud** (CloudKit — container privado `iCloud.br.com.renatoferraz.pontocerto`), para sincronizar entre seu iPhone, iPad, Mac, Apple Watch e Widget.
- O desenvolvedor **não tem acesso** a esses dados. Eles trafegam entre seus próprios dispositivos via infraestrutura da Apple, protegida pela conta iCloud pessoal do usuário.
- **Não usamos** SDKs de terceiros, analytics, rastreamento, anúncios ou publicidade.
- **Não vendemos, alugamos ou compartilhamos** dados com ninguém, porque não os recebemos em primeiro lugar.

---

## 2. Dados tratados pelo app

### Dados que você insere

- Horários de entrada/saída registrados manualmente ou via alarme.
- Configuração de jornada, ciclo mensal, feriados e pausas.
- Preferências de alarme e notificação.

### Dados coletados automaticamente pelo sistema (não pelo desenvolvedor)

- O app usa AlarmKit e Notificações locais do iOS/watchOS para disparar avisos de horário — esses dados de agendamento ficam no próprio sistema operacional do seu dispositivo.
- Nenhum identificador de publicidade, dado de uso agregado ou telemetria é coletado.

### O que o app NÃO coleta

- Não exige criação de conta (login é feito apenas com o Apple ID já configurado no seu dispositivo, para uso do iCloud).
- Não coletamos e-mail, nome, localização, contatos, fotos, dados de saúde ou qualquer identificador pessoal além do necessário pro funcionamento do CloudKit, que é gerenciado pela própria Apple.
- Não rastreamos você entre apps ou sites.

---

## 3. Como os dados são armazenados e sincronizados

- **Armazenamento local:** Core Data, no armazenamento protegido do próprio iOS/iPadOS/macOS/watchOS.
- **Sincronização:** CloudKit, usando o **container privado** da sua conta iCloud. Isso significa que os dados sincronizados só existem dentro do espaço do seu Apple ID — o mesmo mecanismo usado por apps como Lembretes ou Notas da Apple.
- **Widget e Apple Watch:** leem os mesmos dados através de um App Group local (`group.br.com.renatoferraz.pontocerto`) e do CloudKit privado — não há transmissão para fora do ecossistema Apple do próprio usuário.
- O desenvolvedor não opera, não acessa e não tem meio técnico de acessar o conteúdo do seu container CloudKit privado.

---

## 4. Compartilhamento de dados

Não compartilhamos dados com terceiros, porque não os recebemos. A única "parte" envolvida no armazenamento e sincronização, além do seu próprio dispositivo, é a infraestrutura da Apple (iCloud/CloudKit), regida pela [Política de Privacidade da Apple](https://www.apple.com/legal/privacy/br/).

Podemos vir a divulgar informações apenas se exigido por lei ou ordem judicial válida — o que, na prática, não é tecnicamente possível para dados que não passam pelo desenvolvedor.

---

## 5. Segurança

- Os dados no dispositivo seguem a criptografia padrão do iOS/macOS/watchOS.
- Os dados sincronizados via CloudKit seguem a criptografia em trânsito e em repouso da própria Apple.
- Nenhum método de armazenamento é 100% seguro, mas como não existe servidor do desenvolvedor no meio, a superfície de risco fica limitada ao seu próprio dispositivo e à sua conta Apple — cuja segurança é sua responsabilidade (senha forte, autenticação de dois fatores).

---

## 6. Seus direitos e controle (LGPD)

Como o app não envia dados a servidores do desenvolvedor, o controle sobre seus dados é, na prática, total e direto:

- **Acesso e exportação:** todos os seus dados estão visíveis no próprio app, a qualquer momento.
- **Correção:** você pode editar qualquer registro diretamente no app.
- **Exclusão:** apagar o app ou os registros dentro dele remove os dados do dispositivo; desligar a sincronização do iCloud para o app (Ajustes do iPhone > [seu nome] > iCloud) remove os dados do CloudKit.
- **Portabilidade:** os dados ficam na sua conta iCloud, sob seu controle total, independente do desenvolvedor.

Como não somos controladores de um banco de dados central, não há dado nosso para excluir mediante solicitação — a exclusão é feita diretamente por você, no app ou nas configurações do seu Apple ID.

Em caso de dúvidas sobre tratamento de dados pessoais nos termos da Lei Geral de Proteção de Dados (LGPD — Lei nº 13.709/2018), entre em contato pelo e-mail abaixo.

---

## 7. Crianças

O PontoCerto não é direcionado a crianças. É um app de controle de jornada de trabalho, destinado a usuários maiores de 18 anos ou em idade legal de trabalho.

---

## 8. Alterações nesta política

Podemos atualizar esta Política de Privacidade quando o app ganhar novos recursos que mudem o tratamento de dados. A data de "Última atualização" no topo será revisada, e alterações relevantes serão comunicadas dentro do próprio app.

---

## 9. Contato

Dúvidas sobre esta Política de Privacidade:

- **E-mail:** renatodesenv@icloud.com
- **Desenvolvedor:** Renato Ferraz
