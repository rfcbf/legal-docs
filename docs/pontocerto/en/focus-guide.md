---
title: Set up automatic Focus
lang: en
---

# Set up automatic Focus

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

## What this integration does

When you confirm a clock-in, a break, or a clock-out in PontoCerto, the app can turn the **Work** Focus on your iPhone, iPad, or Mac on or off by itself — and when turning it off, it restores whatever Focus was active before (if any).

<img class="shot-mac" style="display:block;margin:1rem auto;max-width:100%;" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-mac-en.jpeg' | relative_url }}" alt="The 'Turn On Work Focus' Shortcut editor showing the whole flow: get the current Focus, save it to a file, and turn Work Focus on" loading="lazy">

This page walks through getting that working, from scratch to tested.

## Before you start

- The **Shortcuts** app needs to be installed (it ships by default on iOS, iPadOS, and macOS).
- **iCloud Drive** needs to be on — the Shortcuts use a small file there to remember which Focus was active before.

Where to start:

- Nothing set up yet → start at **Part 1**.
- Already have the Work Focus, just need the Shortcuts → skip to **Part 2**.
- Already set everything up and it's not working → jump to [Common issues](#common-issues).

## Part 1 — Turn on the "Work" Focus

**1.** Open **Settings > Focus** (on Mac, **System Settings > Focus**) and tap the **Work** Focus — it's already suggested by the system, so you usually don't need to create anything.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-iphone-en.jpeg' | relative_url }}" alt="Settings > Focus screen with the Work Focus highlighted in the list" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-ipad-en.jpeg' | relative_url }}" alt="Settings > Focus screen with the Work Focus highlighted in the list" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/ajustes-foco-lista-mac-en.jpeg' | relative_url }}" alt="Settings > Focus screen with the Work Focus highlighted in the list" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**2.** If **Work** isn't in the list, tap the **+** (on Mac, the **"Add Focus…"** button) and pick **Work** from the suggestions.

> **Never pick "Custom".** A custom Focus gets its own identity, separate from the system's built-in Work Focus — and the Shortcut is set up to turn on that exact system Focus. A custom Focus with the same name won't work.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-iphone-en.jpeg' | relative_url }}" alt="New Focus panel with Custom highlighted as the option to avoid" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-ipad-en.jpeg' | relative_url }}" alt="New Focus panel with Custom highlighted as the option to avoid" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/ajustes-foco-adicionar-mac-en.jpeg' | relative_url }}" alt="New Focus panel with Custom highlighted as the option to avoid" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

If your device is in Portuguese, this same Focus is called **Trabalho** — it's the same one, the system just translates the name. No need to touch anything in the Shortcuts because of that.

## Part 2 — Install the Shortcuts

**3.** In PontoCerto, open **Settings > Focus** (on Mac: **Settings > Alarm & Reminders**, scroll to the Focus section). Turn on **Enable/disable Focus** and tap **Add** on both shortcuts.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-iphone-en.jpeg' | relative_url }}" alt="Focus section in PontoCerto Settings, with the toggle on and the two Add Shortcut buttons" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-ipad-en.jpeg' | relative_url }}" alt="Focus section in PontoCerto Settings, with the toggle on and the two Add Shortcut buttons" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/pontocerto-ajustes-foco-mac-en.jpeg' | relative_url }}" alt="Focus section in PontoCerto Settings, with the toggle on and the two Add Shortcut buttons" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**4.** Confirm on the sheet that opens in the Shortcuts app.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-iphone-en.jpeg' | relative_url }}" alt="'Add Shortcut' confirmation screen in the Shortcuts app" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-ipad-en.jpeg' | relative_url }}" alt="'Add Shortcut' confirmation screen in the Shortcuts app" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalhos-tela-adicionar-mac-en.jpeg' | relative_url }}" alt="'Add Shortcut' confirmation screen in the Shortcuts app" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**5.** In **Shortcuts > All Shortcuts**, check that the names are exactly `Ativar Foco Trabalho` and `Desativar Foco Trabalho`. If it came in with a number at the end (like "Ativar Foco Trabalho 2"), rename it — PontoCerto needs the exact name to call the right shortcut.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalhos-lista-iphone-en.jpeg' | relative_url }}" alt="All Shortcuts list with Ativar Foco Trabalho and Desativar Foco Trabalho highlighted" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalhos-lista-ipad-en.jpeg' | relative_url }}" alt="All Shortcuts list with Ativar Foco Trabalho and Desativar Foco Trabalho highlighted" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalhos-lista-mac-en.jpeg' | relative_url }}" alt="All Shortcuts list with Ativar Foco Trabalho and Desativar Foco Trabalho highlighted" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

**The names stay in Portuguese even with the device in English** — don't translate them.

On Mac, both shortcuts usually show up there already, synced from the iPhone — no need to import them again. If they're not there, import them using the same buttons from step 3, now in the Mac's Shortcuts app.

## Part 3 — Check the "Set Focus" action

**6.** Open each shortcut and check the **Set Focus** action at the end. In "Ativar" (turn on), it should be set to **Work**, turning on. If the field is empty (common when the Focus was created after the shortcut), tap it and pick **Work** again.

<div class="platform-shot">
  <figure class="platform-fig platform-iphone">
    <img class="shot-iphone" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-iphone-en.jpeg' | relative_url }}" alt="'Ativar Foco Trabalho' Shortcut editor with the Set Focus action set to Work" loading="lazy">
    <figcaption>iphone</figcaption>
  </figure>
  <figure class="platform-fig platform-ipad">
    <img class="shot-ipad" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-ipad-en.jpeg' | relative_url }}" alt="'Ativar Foco Trabalho' Shortcut editor with the Set Focus action set to Work" loading="lazy">
    <figcaption>ipad</figcaption>
  </figure>
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalho-definir-foco-mac-en.jpeg' | relative_url }}" alt="'Ativar Foco Trabalho' Shortcut editor with the Set Focus action set to Work" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

<div class="platform-shot">
  <figure class="platform-fig platform-mac">
    <img class="shot-mac" src="{{ '/pontocerto/assets/foco/atalho-seletor-foco-mac-en.jpeg' | relative_url }}" alt="Focus picker open over the Set Focus action, with Work checked" loading="lazy">
    <figcaption>Mac</figcaption>
  </figure>
</div>

In "Desativar" (turn off), there are two Set Focus actions: the first turns Work off (check it the same way as above), and the second uses a variable to restore the previous Focus — **leave that one alone**.

This is just a 15-second check, not a fix — it takes less time than reading this paragraph.

## Part 4 — Test it

**7.** Run the **"Ativar Foco Trabalho"** shortcut manually once, straight from the Shortcuts app. This creates the file that remembers the previous Focus and triggers the permission prompts — without this step, "Desativar" fails the first time it runs.

**8.** Log a clock-in in PontoCerto. The Shortcuts app should flash on screen for a moment and bring you back to PontoCerto by itself.

## Multiple devices

With **"Share Across Devices"** turned on in Settings > Focus, the Work Focus follows all your devices automatically, and the Shortcuts sync through iCloud. Set it up on one device and it's set up on the others — just turn the toggle on in PontoCerto on each one.

## Common issues

| Symptom | Likely cause | Fix |
|---|---|---|
| I confirm a clock-in and Shortcuts doesn't even open | The integration is turned off | Settings > Focus → turn the toggle on |
| Shortcuts says the shortcut doesn't exist | The name doesn't match exactly | Rename it to the exact name — check for a numeric suffix or an accidental rename |
| It runs, but the Focus doesn't change | You created a custom Focus named "Trabalho" | Use the system-suggested Work Focus instead; delete the custom one |
| I get stuck in the Shortcuts app, PontoCerto doesn't come back | The shortcut failed partway through | Run it manually to see where it errors — see the two rows below |
| "Desativar" fails the first time | The file that remembers the previous Focus doesn't exist yet | Run "Ativar" manually once (Part 4) |
| Both shortcuts fail at a file step | iCloud Drive is off or missing permission | Turn on iCloud Drive and accept access to the Shortcuts folder |
| Turning off restores an odd Focus | The restore step uses the previous Focus's name | Expected behavior; turn it off manually from Control Center |
| Works on iPhone, not on Mac | Shortcuts or Focus haven't synced | Turn on "Share Across Devices" and check Shortcuts on the Mac |
| Two "Work" Focuses show up in the list | The built-in one plus an old custom one | Delete the custom one |

## Turning it off

Settings > Focus → turn off the **Enable/disable Focus** toggle. If you want, you can also delete both shortcuts in the Shortcuts app — PontoCerto will simply stop trying to call them.
