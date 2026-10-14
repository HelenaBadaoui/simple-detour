# Simple Detour

> Sur un trajet à pied de A à B, trouve parmi mes adresses Mapstr les lieux qui rallongent le moins mon chemin.

**Simple Detour** est un side project de Product Manager, construit de A à Z avec des outils d'IA (Claude, Lovable, Claude Code). Le but est double : résoudre un vrai besoin personnel et s'entraîner à la démarche produit complète, de la découverte du problème jusqu'à la mesure des résultats.

> **Projet d'entraînement.** L'utilisateur, c'est moi, et c'est assumé. L'objectif n'est pas de valider un marché mais de pratiquer la démarche produit et les outils d'IA, et de documenter chaque choix.

## Le problème

J'ai beaucoup d'adresses sauvegardées sur [Mapstr](https://mapstr.com), avec des tags. Quand je vais d'un point A à un point B, j'aimerais m'arrêter dans l'un de mes cafés (ou autres lieux), à condition que le détour reste minime. Aujourd'hui, je n'ai aucun moyen simple de savoir lesquels sont vraiment sur mon chemin.

## La solution (V1)

À partir d'un point de départ A et d'un point d'arrivée B, Simple Detour :

1. charge mes adresses Mapstr (export CSV ou KML) ;
2. retient les lieux situés près du trajet ;
3. calcule, pour chacun, le temps de marche A → C → B ;
4. classe les lieux par détour, du plus court au plus long, avec le temps ajouté pour chacun.

Le tout est gratuit et pensé pour un usage à pied.

## Périmètre

| V1 | Pistes pour la suite |
|---|---|
| Trajet à pied | Trajets en transport en commun |
| Un seul utilisateur, un seul trajet | Point de rencontre équitable pour plusieurs personnes |
| Classement par détour minimal | Requête en langage naturel appuyée sur mes tags |
| Import d'un export Mapstr | Explication du choix d'un lieu |

Ces éléments sont écartés de la V1 par choix de priorisation, pas par oubli : voir le [journal de décisions](docs/decisions.md).

## À propos des données Mapstr

Je n'ai trouvé aucune API publique chez Mapstr. Le projet repose donc sur l'import d'un export de mes adresses (CSV ou KML), ce qui implique pas de synchronisation automatique.

Simple Detour est un projet indépendant, non affilié à Mapstr.

## Démarche produit

Ce dépôt est aussi un portfolio de la démarche. Les documents sont ajoutés au fil des phases.

| Phase | Contenu | Livrables | Statut |
|---|---|---|---|
| 0. Mise en place | Structure du dépôt et de la documentation | Dépôt, README | En cours |
| 1. Découverte | Problème, journal de mes usages, analyse concurrentielle | `docs/problem.md`, `research/usage-journal.md`, `docs/competitors.md` | À venir |
| 2. Définition | Cadrage, métriques, priorisation, choix d'API | `docs/PRD.md`, `docs/metrics.md`, `docs/roadmap.md`, `docs/decisions.md` | À venir |
| 3. Prototypage | Maquette interactive avec Lovable | `docs/prototype/` | À venir |
| 4. Construction | Développement avec Claude Code, par petites tranches | Code dans `src/` | À venir |
| 5. Lancement et mesure | Usage réel, résultats, rétrospective | `docs/results.md`, `docs/retro.md` | À venir |
| 6. Mise en valeur | README final, publications, récit d'entretien | | À venir |

## Structure du dépôt

```
simple-detour/
├── docs/        # documents produit (PRD, métriques, roadmap, décisions, rétrospective)
├── research/    # journal d'usage et notes de recherche
├── src/         # code de l'application
└── README.md
```

## Stack technique

À définir en phase 2, en fonction des API d'itinéraires à pied disponibles gratuitement et de leurs conditions d'utilisation.

## Lancer le projet

Pas encore disponible : le projet est en cours de construction. Cette section sera complétée au fil de la phase 4.

## Auteur

Projet réalisé par moi-même dans le cadre de ma recherche de poste de Product Manager.
[LinkedIn](https://www.linkedin.com/helena-badaoui)
