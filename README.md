# VeloEurope Studio

## Utilisation

Ouvrez `index.html` dans un navigateur récent : aucun serveur local, Python ou
installation n'est nécessaire pour utiliser l'application. Le HTML contient
les styles, le logo et le code de l'application. Une connexion Internet reste nécessaire
pour charger Leaflet, les fonds de carte et les services de recherche, de
routage, d'altitude, de météo et OpenStreetMap.

- Sur smartphone, la carte reste visible en portrait et en paysage. Utilisez
  **Parcours** pour ouvrir les réglages, puis **Fermer** pour revenir à la
  carte. Les boutons de zoom se trouvent en bas à droite.
- Le bouton **Réseau Véloroutes Europe** affiche les itinéraires et leurs
  références disponibles dans le calque Waymarked Trails/OpenStreetMap. Les
  étiquettes visibles dépendent de la zone, du niveau de zoom et des données
  contributives : tous les itinéraires ne sont pas nécessairement renseignés.
- Le bouton **Voies vertes & pistes** affiche en vert les réseaux de pistes
  et voies cyclables reliées totalisant au moins **3 km** ; les tronçons isolés
  plus courts ne sont pas affichés. Un réseau peut comporter des branches et
  sa longueur cumulée ne garantit pas un trajet unique de 3 km. Zoomez sur la
  zone souhaitée : la recherche couvre au maximum 20 km autour du centre et
  indique si la carte est partiellement couverte ou si le service échoue.
  Les autres fonds et calques, notamment CyclOSM et Réseau Véloroutes Europe,
  ne sont pas filtrés et peuvent montrer des tronçons plus courts. En mode
  dessin, l'accrochage utilise les réseaux verts chargés ; les étapes libres
  restent possibles ailleurs.
- Pour identifier un tracé sans créer d'étape, activez **Identifier une
  véloroute**, zoomez au niveau 10 ou plus et cliquez près de la ligne. Choisissez
  ensuite la relation souhaitée parmi les itinéraires proches. Un même endroit
  peut correspondre à plusieurs références. Désactivez le bouton ou choisissez
  un mode de tracé pour reprendre la création d'étapes.
- La recherche par nom ou référence, par exemple `AV`, `EV3` ou `V40`, permet
  de choisir entre les relations trouvées et d'afficher les pages suivantes.
  Une relation peut représenter une portion, une variante ou un réseau entier.
  Les traits pointillés du catalogue sont des schémas indicatifs ; si la
  recherche d'une entrée du catalogue échoue, l'application précise si un
  trajet a été recalculé entre ses étapes approximatives ou si seul un schéma
  direct provisoire est disponible. Les données OpenStreetMap ne constituent
  pas une certification officielle.
- Les flèches indiquent l'ordre départ-arrivée des itinéraires calculés ou
  dessinés et de leurs variantes. Elles suivent le déplacement et le zoom de la
  carte. Aucun sens n'est inventé pour un réseau OSM dont le sens n'est pas
  indiqué.
- Pour un trajet avec des étapes, jusqu'à **trois propositions distinctes**
  sont recherchées, notamment en dehors du couloir d'une véloroute balisée.
  Sélectionnez une proposition pour afficher ses détails. Le nombre dépend
  des voies et des résultats disponibles ; les aménagements cyclables connus
  sont estimés à partir des étiquettes OSM et ne garantissent pas le terrain.
  Le nettoyage ne supprime pas les étapes explicitement demandées ;
  celui-ci peut toutefois les raccorder au point accessible le plus proche.
- Le calcul active les préférences BRouter pour les véloroutes et l'évitement
  des voies peu sûres (Route/VTC), ou les véloroutes et les estimations de
  circulation (Gravel). Le mode Route pénalise davantage les chemins non
  revêtus. Les variantes BRouter sont prioritaires, puis classées par proportion
  d'aménagements cyclables OSM identifiés, et non simplement par ordre de réponse.
  Les profils rapides ne sont plus recherchés. Le secours OSRM utilise uniquement
  le service vélo ; il est signalé et ses préférences sont moins précises.
  Ces choix peuvent allonger le trajet et ne garantissent ni l'absence de
  nationales ni une faible circulation réelle : vérifiez le parcours avant le départ.
- Pour un trajet **A → B → C**, partout en Europe, les points de guidage posés
  sur une véloroute balisée ne sont pas des étapes obligatoires : s'ils
  provoquent un aller-retour, celui-ci est retiré. Le guidage privilégie les
  EuroVelo et véloroutes nationales ou régionales ; les circuits locaux ne
  servent plus de raccourci. Chaque option indique ses kilomètres sur
  véloroutes balisées (EuroVelo, nationales, régionales) et les options les
  plus balisées sont classées en premier. Une variante est écartée et signalée
  si elle dépasse le trajet le plus court de 35 % (+1,5 km) ; cette marge monte
  jusqu'à 75 % pour une variante entièrement sur véloroute.
  Sur la carte, seule l'option sélectionnée est affichée ; choisissez une autre
  option dans la liste pour l'afficher à la place.
- Pour une **boucle automatique**, les points intermédiaires sont générés par
  l'application : les branches strictement parcourues à l'aller et au retour
  sont supprimées sans inventer de raccord, sauf si elles sont nécessaires à
  une étape ajoutée par l'utilisateur. Ces étapes restent obligatoires. Si la
  distance obtenue s'écarte de plus de 15 % de la
  distance souhaitée, une nouvelle recherche ajuste une fois le rayon ; le
  meilleur résultat est conservé. La distance reste indicative et dépend des
  voies disponibles ; chaque option indique si elle s'écarte de plus de 15 %
  de la distance souhaitée.
- Pour la météo du parcours, choisissez la date et saisissez l'heure de départ
  au format **24 h** (`HH:MM`, par exemple `18:30`).
- Dans **Services & Étapes vélo**, choisissez une catégorie pour rechercher
  les lieux autour du centre de la carte ou à moins de 500 m du parcours actif.
  Cliquez sur un nom pour le voir sur la carte ou sur **+ Étape** pour l'ajouter
  au trajet. Les étapes sont conservées lors du recalcul, y compris pour une
  boucle automatique. Pour un parcours sélectionné sans départ et arrivée
  définis, créez d'abord un trajet A → B ; le mode Explorer ne recalcule pas
  d'étapes. Les résultats peuvent être limités ou incomplets selon les données
  et la disponibilité d'OpenStreetMap.
- La recherche de **Pistes cyclables dans la zone** utilise le rayon autour du
  centre de la carte et affiche uniquement les pistes et voies désignées pour
  les vélos dont les tronçons reliés par des nœuds OpenStreetMap totalisent au
  moins **3 km**. Les traversées cyclables peuvent relier les tronçons, et
  partout en Europe une extrémité de piste située à moins de 60 m d'une autre
  piste est considérée comme reliée (traversée de route ou rond-point non
  cartographié). Les rues cyclables (`cyclestreet`, `bicycle_road`) sont
  incluses. Les
  routes simplement autorisées aux vélos et les bandes sur chaussée ne sont pas
  retenues. Une piste cartographiée le long d'une route peut ne pas avoir de
  géométrie séparée. Un réseau peut comporter des branches : sa longueur
  cumulée n'est pas nécessairement celle d'un trajet unique, et certains
  tronçons retournés par OSM peuvent dépasser le rayon de recherche. La
  continuité et l'accès restent à vérifier sur le terrain.
  La progression et le lien vers les résultats sont visibles sous le curseur.
  Si Overpass est indisponible, une recherche de secours OpenStreetMap est
  limitée à un petit carré autour du centre, indiqué sur la carte et dans la
  liste : un résultat partiel ne prouve pas qu'aucune piste plus longue
  n'existe dans le rayon demandé. Une voie non renseignée dans OSM n'est pas
  nécessairement absente du terrain.
- Un réseau OSM peut contenir des segments disjoints ou des embranchements.
  Dans ce cas, il est affiché par segments, sans parcours, profil ni export GPX
  artificiellement raccordés. Une longueur déclarée dans OSM ou une longueur
  de réseau fournie par Waymarked peut être affichée séparément ; elle peut
  inclure des variantes et n'est pas la distance d'un trajet continu.
  Définissez un trajet A → B pour obtenir distance et dénivelé du parcours choisi.
  Pour une ligne OSM continue dont le sens est inconnu, le D+ estimé dépend de
  l'ordre des points ; l'ordre utilisé dans un GPX n'est pas nécessairement un
  sens balisé. Le dénivelé utilise une estimation altimétrique échantillonnée
  et reste indisponible si le service d'altitude ne répond pas.
- Le bouton **Exporter GPX** enregistre les points du parcours actif dans leur
  ordre, avec les altitudes disponibles.

## Revêtements

La répartition est une **estimation**, jamais une garantie du terrain. Pour
un parcours calculé par BRouter, l'application utilise les étiquettes
OpenStreetMap fournies avec ses tronçons, même si Overpass est indisponible.
Les tronçons modifiés pendant le nettoyage ou associés à des données
contradictoires restent **inconnus**.

Pour les autres parcours, les étiquettes `surface` et le type de voie OSM
sont recherchés par Overpass et rapprochés de la géométrie, par échantillons
de 25 m maximum et à 12 m maximum d'une voie compatible. Si plusieurs voies
de catégories différentes ont des distances au tracé qui diffèrent de 3 m ou
moins, la correspondance reste **inconnue**. Dans tous les cas, une piste
cyclable dont le revêtement n'est pas renseigné reste inconnue : l'application
ne suppose pas qu'elle est asphaltée. Les distances sont calculées sur la
géométrie affichée et peuvent différer légèrement de la distance fournie par
le moteur de routage.

Pour limiter les requêtes publiques, l'analyse est limitée à 200 km de
géométrie par parcours. Au-delà, tout est indiqué comme inconnu : choisissez
une portion plus courte. Un tracé direct provisoire n'est pas analysé.
Utilisez **Actualiser** pour réessayer après une erreur de service. Si
Overpass ne répond pas ou ne trouve aucune correspondance fiable, la dernière
estimation disponible reste affichée.

## Enregistrer et reprendre

**Enregistrer le projet** télécharge un fichier JSON versionné contenant les
étapes, les réglages, la vue de carte, le parcours actif et les variantes
disponibles. **Ouvrir un projet** vérifie le fichier avant de remplacer le
projet actuel. Le parcours et les données déjà enregistrées sont restaurés
sans recalcul de l'itinéraire ; les données externes, telles que la météo,
peuvent ensuite être actualisées. Enregistrez manuellement avant de fermer
l'application : la sauvegarde automatique n'est pas activée.
Les anciens projets utilisant le fond « Carte Claire » sont ouverts avec la
carte routière, et ce remplacement est signalé.

Le fichier JSON contient vos coordonnées et peut révéler vos déplacements.
Conservez-le et partagez-le avec précaution. Les recherches, le calcul du
parcours, l'altitude, la météo et l'analyse des revêtements envoient les
coordonnées nécessaires aux services externes correspondants.

La recherche de lieux et des points d'itinéraire utilise Nominatim. Si ce
service est indisponible, la même recherche est envoyée à Photon (Komoot) ;
le recours à ce service alternatif est indiqué dans l'application. Ces services
publics ne garantissent pas leur disponibilité.

## Modifier et reconstruire

Les sources actives sont dans `src_recupere\` ; `index.html` est le fichier
autonome généré. L'ancien dossier `src\` a été conservé séparément car Windows
a signalé un fichier endommagé. Faites vérifier le lecteur avant de réutiliser
ces anciennes sources.

Après modification des sources actives, exécutez depuis ce dossier :

```powershell
python build.py
python build.py --check
```

Cette étape de reconstruction nécessite Python 3 ; elle n'est pas nécessaire
pour ouvrir `index.html`. Une modification directe du HTML généré sera
remplacée lors de la prochaine reconstruction. Les tests de logique peuvent
être lancés dans un navigateur en ouvrant `tests\logic.html`. Les tests
d'intégration, qui chargent une copie de l'application et nécessitent Leaflet,
sont disponibles dans `tests\app.test.html`.
