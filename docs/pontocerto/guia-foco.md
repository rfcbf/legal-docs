---
title: Configurar o Foco automático
lang: pt
---

# Configurar o Foco automático

<div class="platform-tabs" role="tablist" aria-label="Plataforma">
  <button type="button" class="platform-tab" data-platform-btn="iphone" role="tab">iPhone</button>
  <button type="button" class="platform-tab" data-platform-btn="ipad" role="tab">iPad</button>
  <button type="button" class="platform-tab" data-platform-btn="mac" role="tab">Mac</button>
</div>
<script>
(function () {
  var VALID = ["iphone", "ipad", "mac"];
  var STORAGE_KEY = "pontocerto-guia-foco-platform";
  var html = document.documentElement;

  function detectFromUserAgent() {
    var ua = navigator.userAgent || "";
    if (/iPhone/.test(ua)) return "iphone";
    if (/iPad/.test(ua)) return "ipad";
    if (/Macintosh/.test(ua)) {
      return navigator.maxTouchPoints > 1 ? "ipad" : "mac";
    }
    return null;
  }

  function readStored() {
    try {
      var stored = window.localStorage.getItem(STORAGE_KEY);
      return VALID.indexOf(stored) !== -1 ? stored : null;
    } catch (e) {
      return null;
    }
  }

  function readFromUrl() {
    var params = new URLSearchParams(window.location.search);
    var fromUrl = params.get("p");
    return VALID.indexOf(fromUrl) !== -1 ? fromUrl : null;
  }

  function apply(platform) {
    html.setAttribute("data-platform", platform);
    document.querySelectorAll("[data-platform-btn]").forEach(function (btn) {
      var selected = btn.getAttribute("data-platform-btn") === platform;
      btn.setAttribute("aria-selected", selected ? "true" : "false");
    });
  }

  function select(platform, persist) {
    apply(platform);
    if (persist) {
      try { window.localStorage.setItem(STORAGE_KEY, platform); } catch (e) {}
    }
  }

  select(readFromUrl() || readStored() || detectFromUserAgent() || "iphone", false);

  document.addEventListener("click", function (event) {
    var btn = event.target.closest && event.target.closest("[data-platform-btn]");
    if (!btn) return;
    select(btn.getAttribute("data-platform-btn"), true);
  });
})();
</script>

## O que essa integração faz

Quando você confirma a entrada, o intervalo ou a saída no PontoCerto, o app pode ligar ou desligar sozinho o Foco **Trabalho** do seu iPhone, iPad ou Mac — e, ao desligar, restaura o Foco que estava ativo antes (se algum estivesse).

<img class="shot-mac" style="display:block;margin:1rem auto;max-width:100%;" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-mac-pt.jpeg' | relative_url }}" alt="Editor do Atalho 'Ativar Foco Trabalho' mostrando o fluxo completo: obter o Foco atual, salvar num arquivo e ligar o Foco Trabalho" loading="lazy">

Essa página ensina a deixar isso funcionando, do zero até testado.

## Antes de começar

- O app **Atalhos** precisa estar instalado (vem de fábrica no iOS, iPadOS e macOS).
- O **iCloud Drive** precisa estar ligado — os Atalhos usam um arquivinho lá pra lembrar qual Foco estava ativo antes.

Por onde seguir:

- Não tem nada configurado ainda → comece pela **Parte 1**.
- Já tem o Foco Trabalho, falta só os Atalhos → pule pra **Parte 2**.
- Já configurou tudo e não está funcionando → vá direto pra [Problemas comuns](#problemas-comuns).

## Parte 1 — Ative o Foco "Trabalho"

**1.** Abra **Ajustes > Foco** (no Mac, **Ajustes do Sistema > Foco**) e toque no Foco **Trabalho** — ele já vem sugerido pelo sistema, normalmente nem precisa criar nada.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-iphone-pt.jpeg' | relative_url }}" alt="Tela de Ajustes > Foco com o Foco Trabalho destacado na lista" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-ipad-pt.jpeg' | relative_url }}" alt="Tela de Ajustes > Foco com o Foco Trabalho destacado na lista" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-mac-pt.jpeg' | relative_url }}" alt="Tela de Ajustes > Foco com o Foco Trabalho destacado na lista" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**2.** Se **Trabalho** não estiver na lista, toque no **+** (no Mac, no botão **"Adicionar Foco…"**) e escolha **Trabalho** entre as sugestões.

> **Nunca escolha "Personalizado".** Um Foco personalizado recebe uma identidade própria, diferente do Foco Trabalho embutido do sistema — e o Atalho está configurado pra ligar justamente o Foco do sistema. Um Foco personalizado com o mesmo nome não funciona.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-iphone-pt.jpeg' | relative_url }}" alt="Painel de novo Foco com Personalizado destacado como opção a evitar" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-ipad-pt.jpeg' | relative_url }}" alt="Painel de novo Foco com Personalizado destacado como opção a evitar" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-mac-pt.jpeg' | relative_url }}" alt="Painel de novo Foco com Personalizado destacado como opção a evitar" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

Se o seu aparelho estiver em inglês, esse mesmo Foco se chama **Work** — é o mesmo, o sistema só traduz o nome. Não precisa mexer em nada por causa disso.

## Parte 2 — Instale os Atalhos

**3.** No PontoCerto, abra **Ajustes > Foco** (no Mac: **Ajustes > Alarme e lembretes**, role até a seção Foco). Ligue a opção **Ativar/desativar Foco** e toque em **Adicionar** nos dois atalhos.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-iphone-pt.jpeg' | relative_url }}" alt="Seção Foco nos Ajustes do PontoCerto, com o toggle ligado e os dois botões de instalar atalho" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-ipad-pt.jpeg' | relative_url }}" alt="Seção Foco nos Ajustes do PontoCerto, com o toggle ligado e os dois botões de instalar atalho" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-mac-pt.jpeg' | relative_url }}" alt="Seção Foco nos Ajustes do PontoCerto, com o toggle ligado e os dois botões de instalar atalho" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**4.** Confirme na folha que abrir no app Atalhos.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-iphone-pt.jpeg' | relative_url }}" alt="Tela de confirmação 'Adicionar Atalho' no app Atalhos" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-ipad-pt.jpeg' | relative_url }}" alt="Tela de confirmação 'Adicionar Atalho' no app Atalhos" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-mac-pt.jpeg' | relative_url }}" alt="Tela de confirmação 'Adicionar Atalho' no app Atalhos" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**5.** Em **Atalhos > Todos os Atalhos**, confira que os nomes ficaram exatamente `Ativar Foco Trabalho` e `Desativar Foco Trabalho`. Se veio com um número no fim (tipo "Ativar Foco Trabalho 2"), renomeie — o PontoCerto precisa do nome exato pra chamar o atalho certo.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalhos-lista-iphone-pt.jpeg' | relative_url }}" alt="Lista de Todos os Atalhos com Ativar Foco Trabalho e Desativar Foco Trabalho destacados" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalhos-lista-ipad-pt.jpeg' | relative_url }}" alt="Lista de Todos os Atalhos com Ativar Foco Trabalho e Desativar Foco Trabalho destacados" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalhos-lista-mac-pt.jpeg' | relative_url }}" alt="Lista de Todos os Atalhos com Ativar Foco Trabalho e Desativar Foco Trabalho destacados" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**Os nomes ficam em português mesmo com o aparelho em inglês** — não traduza.

No Mac, os dois atalhos normalmente já aparecem sozinhos ali, sincronizados do iPhone — não precisa importar de novo. Se não aparecerem, importe pelos mesmos botões do passo 3, agora no app Atalhos do Mac.

## Parte 3 — Confira a ação "Definir Foco"

**6.** Abra cada atalho e confira a ação **Definir Foco**, no fim. No "Ativar", tem que estar **Trabalho** ligando. Se o campo estiver vazio (comum quando o Foco foi criado depois do atalho), toque nele e escolha **Trabalho** de novo.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-iphone-pt.jpeg' | relative_url }}" alt="Editor do Atalho 'Ativar Foco Trabalho' com a ação Definir Foco selecionando Trabalho" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-ipad-pt.jpeg' | relative_url }}" alt="Editor do Atalho 'Ativar Foco Trabalho' com a ação Definir Foco selecionando Trabalho" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-mac-pt.jpeg' | relative_url }}" alt="Editor do Atalho 'Ativar Foco Trabalho' com a ação Definir Foco selecionando Trabalho" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

<div class="platform-shot">
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalho-seletor-foco-mac-pt.jpeg' | relative_url }}" alt="Seletor de Foco aberto sobre a ação Definir Foco, com Trabalho marcado" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

No "Desativar", tem duas ações de Definir Foco: a primeira desliga o Trabalho (essa você confere igual à de cima) e a segunda usa uma variável pra restaurar o Foco anterior — **essa não se mexe**.

Isso é só uma conferência de 15 segundos, não um conserto — leva menos tempo que ler este parágrafo.

## Parte 4 — Teste

**7.** Rode o atalho **"Ativar Foco Trabalho"** manualmente uma vez, direto pelo app Atalhos. Isso cria o arquivo que guarda o Foco anterior e dispara os pedidos de permissão — sem esse passo, o "Desativar" falha na primeira vez que rodar.

**8.** Bata um ponto no PontoCerto. O app Atalhos deve piscar na tela por um instante e voltar sozinho pro PontoCerto.

## Vários aparelhos

Com **"Compartilhar entre Dispositivos"** ligado em Ajustes > Foco, o Foco Trabalho acompanha todos os seus aparelhos automaticamente, e os Atalhos sincronizam pelo iCloud. Configurou num aparelho, está configurado nos outros — só falta ligar o toggle no PontoCerto de cada um.

## Problemas comuns

| Sintoma | Causa provável | O que fazer |
|---|---|---|
| Confirmo o ponto e o Atalhos nem abre | A integração está desligada | Ajustes > Foco → ligar o toggle |
| O Atalhos diz que o atalho não existe | O nome não bate exatamente | Renomear pro nome exato — confira sufixo numérico ou renomeação acidental |
| Roda, mas o Foco não muda | Você criou um Foco personalizado chamado "Trabalho" | Use o Foco Trabalho sugerido pelo sistema; apague o personalizado |
| Fico preso no app Atalhos, o PontoCerto não volta | O atalho falhou no meio da execução | Rode manualmente pra ver onde erra — veja as duas linhas abaixo |
| "Desativar" falha na primeira vez | Ainda não existe o arquivo com o Foco anterior | Rode "Ativar" manualmente uma vez (Parte 4) |
| Os dois atalhos falham numa etapa de arquivo | iCloud Drive desligado ou sem permissão | Ligue o iCloud Drive e aceite o acesso à pasta do Atalhos |
| Ao desligar, volta pra um Foco estranho | A restauração usa o nome do Foco anterior | Comportamento esperado; desligue manualmente na Central de Controle |
| Funciona no iPhone, não no Mac | Falta sincronizar Atalhos ou Foco | Ligue "Compartilhar entre Dispositivos" e confira o Atalhos do Mac |
| Aparecem dois Focos "Trabalho" na lista | O embutido e um personalizado antigo coexistindo | Apague o personalizado |

## Como desligar

Ajustes > Foco → desligue o toggle **Ativar/desativar Foco**. Se quiser, também pode apagar os dois atalhos no app Atalhos — o PontoCerto simplesmente para de tentar chamá-los.
