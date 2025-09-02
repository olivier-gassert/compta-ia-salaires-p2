# compta-ia-salaires-p2

Ce projet vise à automatiser la génération d'écritures comptables à partir de documents PDF tels que les fiches de paie, en combinant vision par ordinateur et traitement de texte.

## Partie 2 : Reconnaissance des fiches de paie

La seconde étape du projet consiste à utiliser le modèle précédent dans un notebook basé sur **LayoutLMv3** (Hugging Face), avec des annotations plus précises et un apprentissage par transfert.

---

## Objectifs de cette seconde partie

-  Explorer l’utilisation de **LayoutLMv3**, un modèle orienté documents, en remplacement d’**EfficientNetB0** (CNN).
-  Tester la possibilité de **réutiliser les poids** issus du premier apprentissage supervisé.
-  Approfondir l’annotation des fiches de paie afin d’obtenir un niveau de détail plus adapté à un modèle de type Transformer.


---

## Difficultés rencontrées

-  **Changement de modèle** : passer d’EfficientNetB0 à LayoutLMv3 a nécessité une adaptation plus longue que prévu (différences de structure et de flux d’entrée).
-  **Format des annotations** : les données n’étaient pas en format BERT-like. Une conversion aurait été nécessaire, mais n’a pas pu être réalisée dans les délais impartis.
-  **Poids non intégrés** : certaines cellules prévues pour l’intégration des poids du premier apprentissage ont été mises de côté, en attendant une version stabilisée du nouveau modèle.


---

## Points positifs

-  L’apprentissage avec LayoutLMv3 **fonctionne** malgré les contraintes techniques et de temps.
-  La démarche exploratoire a permis de mieux comprendre les besoins en annotations et la logique des modèles Hugging Face.


---

## Prochaines étapes

-  Exécuter les notebooks en local (Jupyter) pour ne plus dépendre de Google Colab et de GPU externes.
-  Améliorer le dataset :
    * augmenter le nombre de fiches de paie,
    * enrichir la qualité et la précision des annotations.
-  Expérimenter d’autres approches d’apprentissage.


---

##  Données utilisées

Les images utilisées dans ce projet proviennent de deux sources :

-  Un dataset personnel que j'ai créé, comprenant :
	Fiches de paie fictives (au format JPEG)
	Annotations associées (au format JSON)

➡️ Ces données peuvent être utilisées à des fins non commerciales.  
➡️ Je dispose d'autres exemples disponibles sur demande.  
➡️ Je serais reconnaissant si vous me citez si vous utilisez ce dataset, mais cela reste facultatif.

-  Le dataset FUNSD : [https://guillaumejaume.github.io/FUNSD/](https://guillaumejaume.github.io/FUNSD/)

➡️ Le dataset FUNSD est fourni à des fins non commerciales.  
➡️ Les annotations utilisées dans ce projet sont personnelles et ne proviennent pas du dataset original.

##  Merci de citer :

@inproceedings{jaume2019,  
    title = {FUNSD: A Dataset for Form Understanding in Noisy Scanned Documents},  
    author = {Guillaume Jaume, Hazim Kemal Ekenel, Jean-Philippe Thiran},  
    booktitle = {Accepted to ICDAR-OST},  
    year = {2019}  
}

##  Citation suggérée :

@dataset{Gassert2025,  
    author = {Olivier Gassert},  
    title = {Échantillon de dataset de fiches de paie fictives},  
    year = {2025},  
    note = {Disponible dans le projet GitHub : Compta-IA-salaires-p1}  
}
