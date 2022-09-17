Suite aux [discussions sur le formualire « 2020 »](https://forum.cen-occitanie.org/t/formulaire-general-sicen-2020/123) une [série d’améliorations ont été apportées 2](https://forum.cen-occitanie.org/t/formulaire-general-sicen-2020/123/43) au formulaire « Sicen » et c’est la version 14 de TaxRef qui est intégrée et que vous retrouverez dans les listes.

Voici donc un tutoriel, sous forme de captures d’écrans, allant de la configuration d’ODK Collect à la fin de la saisie d’une donnée dans le formulaire.

**!!! A noter !!!**  
Les données collectées de cette version du formulaire alimenteront la base de données SiCen Occitanie dont vous aurez rapidement des nouvelles.

## Évolution technique d’ODK

Avant de commencer, un (tout petit) peu de contexte technique.  
ODK a remplacé le serveur Aggregate par un serveur plus moderne appelé Central. Cela est transparent pour vous mais entraîne quelques changements dans l’usage que vous faites de Collect. La mise à jour des formulaires sur votre téléphone est désormais automatique, tout comme l’envoi des données finalisées au serveur.

Pour ce qui concerne les géomaticiens, Central nous permet de gérer des groupes d’utilisateurs qui accèdent à différents formulaires (Bénévoles, prestataires, partenaires…).

Enfin, un des gros avantages de Central réside dans le fait que les formulaires réalisés pour vos téléphones sont aussi diffusés sous la forme de formulaires web (à ouvrir dans un navigateur), utilisables eux aussi en mode déconnecté. Nathalie reviendra bientôt vers nous avec un formulaire téléphone et web.

Nous pouvons donc désormais utiliser ODK pour lancer des enquêtes web participatives, ou des sondages relatifs à un évènement particulier, en remplacement des framaforms et autres limesurvey.

# Revenons à Sicen.

## Installation et configuration d’ODK Collect

### Installation

Depuis le « playstore » d’Android ou depuis le fichier .apk mis à disposition sur le site du projet : [Release ODK Collect v2022.2.1 · getodk/collect · GitHub 8](https://github.com/getodk/collect/releases/latest)

Un fois téléchargé sur le téléphone (n’importe où), vous cliquez sur le fichier apk pour lancer l’installation. Android mettra tout au bon endroit. Vous pourrez ensuite supprimer le fichier .apk.

![Capture d’écran du 2021-03-18 16-50-05](./fichiers/SicenODK/ecrans/83740995f47b0f1b5f5a167a9ab1891588257388.png) 8](https://github.com/getodk/collect/releases/latest)

### Configuration de l’application

\*\*Important : \*\*  
pour éviter des conflits avec les formulaires vierges déjà enregistrés sur le téléphone et des soucis d’envoi de données.  
Commencez par supprimer les formulaires vierges existants d’ODK avant de le configurer
                                                     
#### Cliquer sur « supprimer formulaire enregistré »

![Screenshot_2021-03-31-19-46-55](./fichiers/SicenODK/ecrans/44016f45a86768d16ab186245f100e5c1bc4a926_2_281x500.png)

#### Dans l’onglet « Formulaires vierges » , Sélectionnez tout et supprimez

![Screenshot_2021-03-31-19-47-02](./fichiers/SicenODK/ecrans/8646096ad129d96a0f9aa7eb30c9020c20935775_2_281x500.png)

Tout d’abord, la connexion au serveur de formulaires (nommé Central) se fait par le scan d’un QRcode.  
Vous avez deux possibilités (et deux QRCode au choix):

* soit ODK Collect gère automatiquement
    * le téléchargement des nouvelles formulaires disponibles (tous)
    * de leurs nouvelles versions
    * l’envoi des données des formulaires finalisés au serveur
* soit vous faites cela à la demande
    * télécharger les formulaires qui vous intéressent
    * télécharger les nouvelles versions
    * envoi des données au serveur

Les Qrcode ci-dessous sont destinés aux membres de l’équipe du CEN et n’ont pas à être utilisés par les partenaires ou bénévoles qui auront le leur.

### QRCode « salariés »

![Capture d’écran du 2021-03-19 11-22-50](./fichiers/SicenODK/ecrans/4156acd5b9e7c977be29426010bcd131efe73f3c.png)

### QRCode « stagiaires »

![QRCode_Stagiaire_CEN_managed](./fichiers/SicenODK/ecrans/ca83a848ffed400596ac9f49d632bfea4396f16b.png)

#### Paramètres

![Screenshot_2021-03-11-15-28-03-576x1024](./fichiers/SicenODK/ecrans/25a1726c56451e86add3da7457de93a574756ed4_2_281x500.png)

#### Configurer par QRCode

![Screenshot_2021-03-11-12-16-39-576x1024](./fichiers/SicenODK/ecrans/6570e49d139731d8718f67f9aaace6b5d6759fbe_2_281x500.png)

Une fois le code scanné, votre application est configurée et interroge le serveur pour savoir quels formulaires sont disponibles, et les télécharge.

#### Identité de l’utilisateur

Il nous faut maintenant renseigner les données d’identification qui permettront de vous faire connaître une fois pour toutes dans les différents formulaires et de vous attribuer correctement vos données.

→ Veillez à renseigner l’adresse mail (_**!!! votre adresse professionnelle en minuscules !!!**_).

![identite_utilisateur-576x1024](./fichiers/SicenODK/ecrans/2c6b6484f465edafa797c37ab51dbf229d89b6ae_2_281x500.png)
![metadonnees_de_formualire-576x1024](./fichiers/SicenODK/ecrans/d48fad63dbd77895fb21af0fccdb519f096a4892_2_281x500.png)
![Screenshot_2021-03-11-12-17-54-576x1024](./fichiers/SicenODK/ecrans/2d267abdce7d8312dbc6430a5fc2d361d9aca632_2_281x500.png)

#### Cartes → Choisir Mapbox

![Screenshot_2021-03-18-15-42-00](./fichiers/SicenODK/ecrans/2567e0a9272a95474efdb3de22e7d28c56d17e94_2_281x500.png)

#### Autres paramètres utiles

De retour sur l’écran des paramètres, vous pourrez modifier :

* la taille de la police qui sera utilisée dans les formulaires
* la manière de naviguer d’un écran à l’autre
    * en faisant glisser le doigt sur l’écran de gauche à droite pour avancer et de droite à gauche pour reculer
    * en affichant des boutons en bas de l’écran
    * en utilisant les deux méthodes

Vous êtes maintenant prêts à saisir votre premier formulaire.  
ODKCollect est configuré pour proposer systématiquement les dernières versions des formulaires disponibles sur le serveur.

## Saisie de données

Sur la page d’accueil de l’application, cliquons sur **Remplir un formulaire**

Choisissons **Sicen**

![Screenshot_2021-03-15-16-19-30](./fichiers/SicenODK/ecrans/e9cd90278941d4ed54c8a648be9829707dba48a6_2_281x500.png)

Les 3 premiers écrans vous présentent le paramétrage de l’application. A la première utilisation, les fonctionnalités seront toutes activées par défaut. Libre à vous de désactiver celles qui vous semblent provisoirement ou définitivement inutiles.  
A l’utilisation suivante, chacune des fonctionnalités sera proposée dans l’état d’activation qui était le sien lors de votre dernière utilisation. Vous pourrez là encore valider ou modifier chacun de ce choix.  
Les fonctionnalités désactivées ici seront masquées pendant votre utilisation du formulaire.

### Écran de paramétrage n°1 → l’identité de l’utilisateur

Les champs sont remplis par défaut avec les valeurs saisies dans les paramètres généraux de l’application (voir début de ce tutoriel)

![Screenshot_2021-03-15-16-19-36](./fichiers/SicenODK/ecrans/3c214c32ad4a8edd598b9f9cbb8c018be3aafeb4_2_281x500.png)

### Écran de paramétrage n°2 → types de géométries créées

* points
* lignes
* polygones

![Screenshot_2021-03-15-16-20-24](./fichiers/SicenODK/ecrans/8f81d5ce15d72f30c15a392d0aff4fa414043f97_2_281x500.png)

### Écran de paramétrage n°3 → Types de données (thématiques) et paramétrage de l’autocomplétion

La dernière question vous permet de choisir le nombre de caractères à saisir dans le recherche des espèces avant de déclencher l’interrogation du référentiel. 3 est le minimum, 7 le maximum (pour permettre l’utilisation du « code taxon » par exemple « ERI RUB »)

![Screenshot_2021-03-18-14-27-44](./fichiers/SicenODK/ecrans/b5e63ec58773155174846b0994da66cca11de896_2_281x500.png)

Une fois les paramétrages vérifiés et ou modifiés vous pouvez

### Choisir l’étude

A terme nous aimerions générer dynamiquement et régulièrement cette liste d’études pour ne faire apparaître que les études en cours et pourquoi pas que celles qui concernent l’utilisateur de l’application

![Screenshot_2021-03-15-16-20-32](./fichiers/SicenODK/ecrans/07fc4a90333dabc73b93f67a370a25bf6ffa008c_2_281x500.png)

#### Choisir le protocole

Ici aussi, nous devrions pouvoir limiter la liste des protocoles selon l’étude choisie ou l’utilisateur de l’application.

![Screenshot_2021-03-15-16-20-35](./fichiers/SicenODK/ecrans/35518d4bff33039dbf5ccbb04770e6682207d8f4_2_281x500.png)

Une fois ces paramètres de « session » renseignés, nous pouvons commencer la saisie de données proprement dite.

### Création d’une localité

Il s’agira d’un point, d’une ligne ou d’un polygone.


![Screenshot_2021-03-15-16-20-39](./fichiers/SicenODK/ecrans/69ef697b1d57549190f285ec4527fecf2fd02410_2_281x500.png)

Le GPS peux vous aider à dessiner automatiquement lignes et contours, que vous pouvez aussi dessiner à la main sur l’écran.

![Screenshot_2021-03-15-16-20-45](./fichiers/SicenODK/ecrans/65909728c11fb5d5378d822a8bfdfccd5c751f18_2_281x500.jpeg)

![Screenshot_2021-03-15-16-20-49](./fichiers/SicenODK/ecrans/cdee3385f0f28311eb7809f26d16eb5269fc0b8b_2_281x500.png)

### Saisie d’une ou plusieurs observations à cet endroit

Une fois l’emplacement créé, nous allons pouvoir y créer autant d’observations que nous le souhaitons, de chacun des types d’observations autorisés dans les paramétrages du formulaire.  
« **Pression / menace** » vous permettra de localiser et documenter une pression ou une menace sur le milieu.  
« **Observation générale** » correspond aux jalons que vous connaissez dans Orux Maps, MapInr…, et permet de prendre une photo géolocalisées, que vous pourrez surcharger et commenter.  
Ces observation sont aussi mobilisables dans QGIS.

![Screenshot_2021-03-15-16-20-59](./fichiers/SicenODK/ecrans/d0ac0841e88065db02ded37eeb3e93568ee93a13_2_281x500.png)

Commençons par une espèce végétale

![Screenshot_2021-03-15-16-21-03](./fichiers/SicenODK/ecrans/58fd2ea7ab6fba89619d4c96b552de9686601c5d_2_281x500.png)

### Propositions des taxons de référence et des synonymes qui correspondent aux lettres tapées

D’abord les taxons de rangs supérieurs puis les espèces et sous espèces.

![Screenshot_2021-03-15-16-21-12](./fichiers/SicenODK/ecrans/3ab7bbdb1b1f4b4b69d254e0d274e400eb0d0a54_2_281x500.png)

On peut aussi utiliser un code espèce compose ds 3 premières lettres du Genre et des 3 premières de l’espèce et le cas échéant des 3 premières de la sous-espèce :  

![bc2e8491ac46b81a4526453e20075d657f60b167](./fichiers/SicenODK/ecrans/bc2e8491ac46b81a4526453e20075d657f60b167_2_281x500.png)
#### Renseignement de l’effectif observé

Pour clarifier la collecte de données d’absence, nous avons ajouté une question explicite :  
Si le taxon n’a pas été vu, c’est qu’il était recherché et absent. Dans ce cas les questions relatives à la saisie de l’effectif ne seront pas affichée.  

![Screenshot_2021-03-29-12-41-58](./fichiers/SicenODK/ecrans/f35f4ac85de8cb544a6b9e12f1cbff241ff0b3e6_2_281x500.png)

Mais si l’espèce a été observée, les écrans suivant (ou leurs homologues pour la Faune sont affichés)

Ici pour les espèces végétales il s’agit d’un effectif par classes d’abondance

![Screenshot_2021-03-15-16-21-18](./fichiers/SicenODK/ecrans/f3d3b681a63728d70ef386f0650eec9a243a46ef_2_281x500.png)

### Informations sur la « qualité » de la donnée

Notez que l’observation pourra être retrouvée dans la navigation du formulaire, avec l’heure de l’emplacement et l’espèce observée.

![Screenshot_2021-03-15-16-21-23](./fichiers/SicenODK/ecrans/5b59994a5cc1fc05f4f119718822075008e581be_2_281x500.png)

![Screenshot_2021-03-15-16-21-27](./fichiers/SicenODK/ecrans/0edbdd316c1162c3d4b3d0584f3e984250ba22d0_2_281x500.png)

### Renseignement de détails optionnels, prise de photo

![Screenshot_2021-03-15-16-21-33](./fichiers/SicenODK/ecrans/b9643312d5dcdd1757c0c57a1295c034cee49aee_2_281x500.png)

![Screenshot_2021-03-15-16-21-36](./fichiers/SicenODK/ecrans/c1a6e76f2cf96d2364fa95e091eef8164cf2c825_2_281x500.png)

![Screenshot_2021-03-15-16-22-19](./fichiers/SicenODK/ecrans/ae356edc1ffb76b7ed3afe08cb5e4a55440e39f6_2_281x500.jpeg)

### Annotation de la photo

Cela peut être utile pour les photos de site dans le cas d’observations de type pression/menace  
[Photos mobilisables dans QGIS par la suite](https://si.cen-occitanie.org/?p=191)

![Screenshot_2021-03-15-16-22-38](./fichiers/SicenODK/ecrans/f29eb2f61b3934b24959d097cd34cdcc6fcaae77_2_690x388.jpeg)

![Screenshot_2021-03-15-16-22-48](./fichiers/SicenODK/ecrans/bbfbdb9fa5891f2586f11b97d57b7ab933af78dc_2_281x500.jpeg)

### ajout d’une observation

Si oui on revient à la saisie d’une observation sur l’emplacement courant.

![Screenshot_2021-03-15-16-22-51](./fichiers/SicenODK/ecrans/b9a39b1b46509f7a79dc43586ea50a657b45119e_2_281x500.png)

Si non il nous est proposé d’ajouter une nouvelle localité

![Screenshot_2021-03-15-16-23-01](./fichiers/SicenODK/ecrans/b592a1c18e3db81b5c6fb56d32d15546eaa150b9_2_281x500.png)

Si oui on revient à l’ajout d’une localité (point, ligne ou polygone)  
Si non, on finalise le formualire en renseignant la présence d’éventuels accompagnateurs

### Renseignement des accompagnateurs éventuels

![Screenshot_2021-03-15-16-23-07](./fichiers/SicenODK/ecrans/a60af1308f69e4b08731770cc49e6a6d3c56f6b7_2_281x500.png)

![Screenshot_2021-03-18-15-31-11](./fichiers/SicenODK/ecrans/30a0e1a7025aa5c8f59b04b5c7fb9ef7cd87fa56_2_281x500.png)

### Modification / révision éventuelle des données saisies

**Au fur et à mesure de la saisie, n’hésitez pas à utiliser l’icône de la disquette pour enregistrer le formulaire en cours sur votre téléphone.**  
L’icône représentant une flèche montrant un point permet de naviguer dans les observations déjà saisie pour les vérifier ou les modifier.

![Screenshot_2021-03-15-16-23-14](./fichiers/SicenODK/ecrans/636d8578d201fae3696786c1ecb50a8e288331c0_2_281x500.png)

![Screenshot_2021-03-15-16-23-16](./fichiers/SicenODK/ecrans/6162622a937abe0231939e3ea228b235ac4d5942_2_281x500.png)

![Screenshot_2021-03-15-16-23-22](./fichiers/SicenODK/ecrans/49ae29153b2a6036ed7d3c43296d98f668c8774b_2_281x500.png)

![Screenshot_2021-03-15-16-23-25](./fichiers/SicenODK/ecrans/7c2349bdb93368fdadc1e0020d5d5e95693d1c38_2_281x500.png)

![Screenshot_2021-03-15-16-23-29](./fichiers/SicenODK/ecrans/9392d2a343f6e224a6d764dc6adb26d67a33ac82_2_281x500.png)

Une fois ceci fait on peut aller au bout du formulaire et le marquer comme finalisé.

### Finalisation du formulaire

![Screenshot_2021-03-15-16-23-51](./fichiers/SicenODK/ecrans/d723bf9f17c065891e34ceb7f2e7c81dda36099c_2_281x500.png)]

## Améliorations apportées pour la saison 2022

* taxref v15 avec un élargissement des statuts biogéographies utilisés
* ajout du déterminateur (par défaut l’observateur)
* ajout par défaut de la valeur ‹ Vu › à la question « détermination »
* possibilité de créer une observation de type « station »
* possibilité de ne pas repasser sur ses préférences pour ne pas voir ces deux écrans au démarrage
* possibilité d’ajouter un nouveau site/étude/protocole si celui qu’il vous faut n’est pas listé.
