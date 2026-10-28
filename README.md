# Cause gaga

Un plugin Claude Code qui fait causer Claude en gaga, le parler populaire de Saint-Étienne, et qui lui fait comprendre quand on lui parle gaga.

C'est un [output style](https://code.claude.com/docs/en/output-styles.md) : des consignes (dosage, tournures, ce qui reste en français standard) et un lexique de 760 entrées, envoyés avec chaque message. Le gaga reste dans la conversation : le code, les commits et les PR s'écrivent comme d'habitude.

## Installer

Dans Claude Code :

```
/plugin marketplace add husur/cause-gaga
/plugin install cause-gaga@cause-gaga
/output-style cause-gaga:gaga
```

Pour revenir au français standard : `/output-style default`.

## Recevoir les mises à jour

Claude Code ne met pas à jour automatiquement les plugins qui ne viennent pas d'Anthropic. Pour l'activer, une fois : `/plugin`, onglet **Marketplaces**, `cause-gaga`, **Enable auto-update**. Chaque nouveau commit arrive alors en arrière-plan, et la session suivante le charge.

Sans ça, à la main : `claude plugin update cause-gaga@cause-gaga`.

## Bon à savoir

- Le lexique pèse environ 70 Ko, envoyés avec chaque message (mis en cache après le premier). Compter une vingtaine de milliers de tokens de contexte.
- Un output style est une consigne, pas une garantie : Claude peut en faire trop ou pas assez. Les sous-agents ne le reçoivent pas.

## Contribuer

Le lexique est dans [`output-styles/gaga.md`](output-styles/gaga.md). Un mot qui manque, un sens faux, une tournure mal rendue : une issue ou une PR, de préférence avec un exemple de phrase.

## Licence

[CC BY-SA 4.0](LICENSE). Le lexique est tiré du [Glossaire du parler gaga](https://fr.wiktionary.org/wiki/Annexe:Glossaire_du_parler_gaga) du Wiktionnaire (révision 39322588 du 25 février 2026), par ses contributeurs, sous la même licence. Il a été converti en Markdown, sans les notes ni les références.
