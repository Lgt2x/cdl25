<h1 class="r-fit-text">Simulation numérique et logiciel libre</h2>

<p class="r-fit-text">Louis Gombert - 15/11/2025 - Campus du Libre, INSA Lyon</p>

---
### $whoami

- Télécom INSA Lyon '23
- Ingénieur R&D @ Kitware
- Associatif: SIA, Cod'INSA, F8KLY...

---
### Simulation numérique, pour quoi ?

<img class="r-stretch" src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/USCAE_Bay_Model_-_San_Francisco_Bay_Detail.jpg/1280px-USCAE_Bay_Model_-_San_Francisco_Bay_Detail.jpg"/>

Modèle 1:1000 de la baie de San Francisco, 1957

<p class="credits">Credits: Wikimedia Commons</p>

Note: https://www.youtube.com/watch?v=i70wkxmumAw

***

### Simulation numérique, pour quoi ?

<img class="r-stretch" src="https://www.aero-ce.com/wp-content/uploads/2022/04/Furtive-eGT-Model-02-680x1024.jpg" />

Soufflerie à Magny-Cours, 250kW

<p class="credits">Credits: Aero concept Engineering</p>

Note: https://www.aero-ce.com/nos-moyens

---

### En somme

- **Modélisation** basée sur des **phénomènes physiques**
- Itérations plus rapides pour les ingénieurs
- **Réduction des coûts** de développement et du risque


---

### Les étapes d'une simulation

<div class="mermaid">
<pre>
    %%{init: {'theme': 'light', 'themeVariables': { 'darkMode': false }}}%%
    flowchart LR
    A[CA0] --> B[Prétraitement]
    B --> C[Simulateur]
    C --> D[Post-traitement]
</pre>
</div>

***

### Les étapes d'une simulation

<div class="mermaid">
<pre>
    %%{init: {'theme': 'light', 'themeVariables': { 'darkMode': false }}}%%
    flowchart LR
    A[CAO] -- représentation paramétrique --> B[Prétraitement]
    B -- Maillage adapté, conditions initiales... --> C[Simulateur]
    C -- Nouvelle géométrie, champs scalaires --> D[Post-traitement]
</pre>
</div>

---

### Dans l'industrie (et les écoles)

- Ecosystèmes propriétaires "tout-en-un"
- Ansys, Autodesk, STAR-CCM+ (Siemens), Simulia (Dassault), COMSOL...

<img class="r-stretch" src="assets/autodesk.png" />

---

<img class="r-stretch" src="assets/yes2.png" />


---

### Pourquoi l'open source?

- Accessibilité
- Interopérabilité
- Extensibilité
- Maîtrise des coûts

---

### Tour d'horizon des logiciels
### open source

---

### CAD: FreeCAD

- Modélisation paramétrique de pièces
- Basé sur les kernels OpenCASCADE
- v1.0.0 sortie il y a 1 an

<p class="credits">License: LGPL</p>

***

![sketch](assets/sketch.png)

Contraintes sur un schéma 2D

***

![pad](assets/pad.png)

Extrusion de la pièce
---

### Pre-processing: GMSH

- Création de maillage raffiné pour la simulation
- Pont depuis FreeCAD
- Module IHM

<p class="credits">License: GPLv2</p>

***

![meshing](assets/meshing.png)

Affinage du maillage volumique à proximité de la voiture

---

### Solveurs

- Beaucoup de diversité et de méthodes!
- CFD: OpenFOAM (GPL), code_saturne (GPL)
- Autres FEM: code_aster (GPL), OpenRadioss (AGPL)
- Nouvelle génération: FEniCS (LGPL)

***

![initial conditions](assets/initial.png)

Définition des méta-données de simulation
***

![boundaries](assets/boundaries.png)

Définition des conditions au limites

***

![of_sim](assets/of_sim.png)

Lancement et suivi en direct
---

### Post-processing: ParaView

- \>100 lecteurs de formats différents
- Visualisation et analyse de données 3D
- Facilement extensible
- Basé sur la bibliothèque VTK

<p class="credits">Disclaimer: je travaille pour l'éditeur de ParaView</p>
<p class="credits">License: BSD-3</p>

***

Affichage des lignes de champ


<video data-autoplay src="assets/analysis.mp4"></video>


---

### Où en sommes-nous ?

- Oui, on peut faire de l'ingénierie basée OSS!
- Surtout pour la recherche, et des cas spécifiques
- Ergonomie et interopérabilité: encore des progrès à faire
- Peu de tentatives de "tout-en-un" (Salome, FreeCAD-CFDOF)

---

### Questions ?

Slides: [slides.f4mkg.fr/cdl25](https://slides.f4mkg.fr/cdl25)

Code: [https://github.com/Lgt2x/cdl25](https://github.com/Lgt2x/cdl25)
