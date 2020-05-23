# Wisconsin cancer (breast cancer) analysis

## Données Diagnostic de cancer Wisconsin (WDBC)
Sources :
  Dr. William H. Wolberg, General Surgery Dept., University of Wisconsin, Clinical Sciences Center, Madison,
  WI 53792, wolberg@eagle.surgery.wisc.eduW. Nick Street, Computer Sciences Dept., University of
  Wisconsin, 1210 West Dayton St., Madison, WI 53706, street@cs.wisc.edu 608-262-6619Olvi L.
  Mangasarian, Computer Sciences Dept., University of Wisconsin, 1210 West Dayton St., Madison, WI
  53706, olvi@cs.wisc.edu
  Date: Novembre 1995
 ### Description :
  Caractéristiques sont calculées à partir d'une image numérisée d'une aiguille fine d’aspiration (FNA) d'une
  masse au sein. Elles décrivent les caractéristiques des noyaux de cellules présentes dans l'image .
  - Champ de prédiction 2 , diagnostic: B = bénigne , M = maligne
  - Ensembles sont linéairement séparables en utilisant les 30 caractéristiques d'entrée
  - Une meilleure précision prédictive obtenue en utilisant un plan de séparation dans l'espace 3D. Précision
  estimée à 97,5 % en utilisant la Crossvalidation 10 fois.
  
  Les résultats décrits ci-dessus ont été obtenus en utilisant la Multisurface Method-Tree (MSM-T) [K. P.
  Bennett, "Decision Tree Construction Via Linear Programming." Proceedings of the 4th Midwest Artificial
  Intelligence and Cognitive Science Society, pp. 97-101, 1992], une méthode de classification qui utilise la
  programmation linéaire pour la construction d'un arbre de décision. Les caractéristiques pertinentes ont
  été sélectionnées en utilisant une recherche exhaustive dans l'espace de 1-4 caractéristiques et 1-3 plans
  de séparation.
  Le programme linéaire utilisé pour obtenir le plan de séparation dans l'espace à 3 dimensions est celui
  décrit dans :
  [K. P. Bennett and O. L. Mangasarian: "Robust Linear Programming Discrimination of Two Linearly
  Inseparable Sets", Optimization Methods and Software 1, 1992, 23-34].
  Nombre de cas : 569
  Nombre d'attributs : 32 (ID, le diagnostic , 30 fonctions à valeurs réelles )
  Information sur les attributs :
  1) le numéro d'identification
  2) Diagnostic ( M = maligne , B = bénigne )
  3) Dix fonctions à valeurs réelles sont calculées pour chaque noyau de la cellule :
    a) rayon (moyenne des distances de centre aux points sur le périmètre)
    b) la texture (écart-type des valeurs de gris)
    c) périmètre
    d) zone
    e) la douceur (variation locale de longueurs de rayon)
    f ) la compacité (périmètre ^ 2 / zone - 1.0)
    g) concavité (gravité des portions concaves du contour) des points (nombre de parties concaves
    du contour)
    h) concaves
    i) la symétrie
    j) la dimension fractale (« approximation du littoral " - 1 )
  Plusieurs des documents mentionnés ci-dessus contiennent des descriptions détaillées sur comment ces
  caractéristiques sont calculées.
  Distribution de classe : 357 bénigne, maligne 212
