# Documentation Technique - Projet Thé Bulle

## Introduction et Nomenclature
Ce projet d'intégration a été réalisé en suivant une approche modulaire et structurée. J'ai choisi d'appliquer la méthodologie **BEM (Block Element Modifier)** pour la nomenclature de mes classes CSS. Ce choix se justifie par la volonté de créer un code auto-explicatif et d'éviter les conflits de spécificité. En isolant les blocs (comme `.team`) de leurs éléments (`.team__grid`), la maintenance du site devient beaucoup plus simple et prévisible, ce qui est essentiel pour un projet évolutif.

## Design Tokens et Organisation CSS
L'harmonie visuelle du site repose sur une gestion centralisée des styles via des **variables CSS** (Design Tokens) déclarées dans le `:root`. Cette logique d'organisation permet de maintenir une cohérence parfaite entre les différentes sections. J'y ai regroupé les palettes de couleurs (notamment l'orange `#F4A261` pour les accents), les polices de caractères et les rayons de bordure. Cette méthode facilite les modifications globales : changer une seule variable met à jour l'ensemble de l'interface instantanément.

## Liste des composants réutilisables
Pour optimiser le code, plusieurs composants ont été conçus pour être réutilisés à travers les différentes sections :

- .btn : Un bouton flexible avec des variantes (--primary, --secondary, --outline).

- .section-title : Standardisation des titres de sections.

- .container : Bloc structurel pour le centrage du contenu.

- .map-marker : Composant de localisation pour les cartes.

## Architecture des Layouts et Flexbox
Pour répondre aux défis de mise en page complexes, j'ai privilégié l'utilisation de **Flexbox**. Dans la section "Équipe", Flexbox a permis de superposer verticalement l'introduction et la grille, tandis que dans le "Footer", il a servi à créer une répartition équilibrée des colonnes d'information. Pour les éléments nécessitant un alignement bidimensionnel rigoureux, comme la grille des membres, j'ai combiné Flexbox avec **CSS Grid** pour obtenir un rendu parfaitement symétrique.

## Fonctions Fluides et Adaptabilité
Afin d'assurer une expérience fluide sans multiplier les media queries, j'ai intégré des fonctions CSS modernes. La fonction `calc()` a été utilisée pour gérer les espacements dynamiques, tandis que la fonction `clamp()` a été appliquée aux tailles de police. Cela permet aux titres de se redimensionner de façon organique entre les formats mobile et desktop, garantissant une lisibilité optimale sur tous les appareils.

## Défis Techniques et Solutions
Le principal défi de cette intégration a été le positionnement des marqueurs de localisation sur les cartes. Pour résoudre ce problème, j'ai utilisé un positionnement `absolute` pour les points d'identification à l'intérieur de conteneurs en `relative`. Cela a permis de placer les épingles précisément sur les coordonnées de la maquette, peu importe la taille de l'écran. Un autre défi concernait la spécificité CSS pour les boutons et titres ; j'ai résolu cela en créant des sélecteurs plus précis incluant la classe de section parente, assurant ainsi que les couleurs de la maquette ne soient pas écrasées par les styles par défaut. De plus, j'ai eu plusieurs problèmes persistants et les voicis : un autre défi technique a été d'ajouter la bonne typographie aux mots associés. Je n'ai malheureusement pas trouvé de solutions à ce problème même en installant la bonne typographie. Certains mots ont une autre typographie que celle qui est associé et d'autres ont une typographie normalle puisque je n'arrivais pas à leurs donner un type de typographie. Un autre problème que j'ai rencontré est celui que je ne suis pas arrivé à mettre la couleur spécifique en arrière plan dans les images dans la section équipes. Je n'ai pas trouvé de solution pour ce problème.

## Utilisation de l'Intelligence Artificielle (IA)
Dans une optique de transparence et de collaboration technologique, j'ai utilisé l'outil suivant pour m'assister dans le développement :
- **Outil :** Gemini 3 Flash (Google), version Web.
- **Date :** 22 mars 2026.
- **Utilisation :** L'IA a été sollicitée pour optimiser la structure de la grille de l'équipe, déboguer l'affichage des fichiers SVG et valider la logique de positionnement des marqueurs sur les cartes. Elle a également aidé à valider certains bouts de code dans le html et le css et à proposer des solutions/astuces pour avoir un meilleur résultat et ne pas être mélangé dans le html et le css.