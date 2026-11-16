# claude-session

Une page relais qui ouvre une session Claude Desktop depuis un lien https.

GitHub retire les liens `claude://` des commentaires d'issues et de PR. Les tâches planifiées y écrivent donc un
lien vers cette page, qui redirige vers la session :

```
https://pgoergler.github.io/claude-session/#local_<identifiant de session>
  → claude://claude.ai/epitaxy/local_<identifiant de session>
```

- L'identifiant est dans le fragment (`#…`), qui n'est jamais envoyé au serveur.
- Seul un identifiant de la forme `local_` + UUID en minuscules est accepté ; sinon la page affiche une erreur et ne
  redirige nulle part.
- La session ne s'ouvre que sur le Mac où elle tourne : sur téléphone, la page le dit sans rediriger.
