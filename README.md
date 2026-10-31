# Usage tracking

Shared admin page for my apps (interface in French): **[marl75.github.io/admin](https://marl75.github.io/admin/)**

- One tab per app: [Collection](https://marl75.github.io/mes-livres/) and [Routine](https://marl75.github.io/fitness-coach/), plus a **Site** tab for [marlenemenoire.com](https://marlenemenoire.com/)
- The Site tab reads the visitors measured by [GoatCounter](https://marlenemenoire.goatcounter.com) (cookieless) through its public counter: no key in the page; the "Allow adding visitor counts on your website" setting must be ticked in GoatCounter
- Each app has its own Firebase project; the page signs in to both with the same email and password
- The statistics (`usage/{uid}` in each project) can only be read by the administrator, thanks to each project's Firestore rules; if access is not authorised yet, the page shows the rules to paste into the Firebase console
- A **Retours** (feedback) tab gathers the « Une idée, un souci ? » ("Got an idea or a problem?") messages sent from the apps (Routine for now: `feedback` collection), with their context (version, screen, language, browser) and a Nouveau / À traiter / Fait (new / to do / done) status
- No data is stored in this repository: the page reads everything live from Firebase
