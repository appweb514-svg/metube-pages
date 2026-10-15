# Journal

- 2026-10-15 | demande | Version de MeTube installable sur GitHub Pages (github.io) sans serveur, avec React. Demande reçue via une session depuis ~/Projets/Dicto (sans rapport avec Dicto).
- 2026-10-15 | décision | Architecture : front React statique + yt-dlp dans GitHub Actions (workflow_dispatch + artefacts). Détails dans DECISIONS.md.
- 2026-10-15 | création dépôt | ~/Projets/metube-pages (git init local, branche feat/metube-pages). Création du dépôt distant GitHub refusée par le système de permissions : pas de remote, pas de PR tant que l'utilisateur ne l'a pas autorisé.
- 2026-10-15 | implémentation | Noyau (client API GitHub, catalogue, jobs), scripts Python (ytdl_opts/ytdl_run/subscriptions_check, 20 tests unittest), workflows (download, deploy-pages, subscriptions, ci), UI React EN/FR avec abonnements (26 tests vitest). Aperçu navigateur vérifié avec une API GitHub simulée (Playwright) : ajout, file, terminés, mobile sombre, abonnements. yt-dlp réel testé en local (audio mp3 et vidéo depuis une URL directe).
- 2026-10-15 | limite | Non testé de bout en bout sur GitHub (dépôt distant non créé : refusé par le système de permissions). CORS du téléchargement d'artefacts, comportement réel de YouTube depuis les runners et quotas non vérifiés.
- 2026-10-15 | dépôt + PR | Dépôt privé appweb514-svg/metube-pages créé, branche feat/metube-pages poussée, PR #1 ouverte (pas de merge). https://github.com/appweb514-svg/metube-pages/pull/1
