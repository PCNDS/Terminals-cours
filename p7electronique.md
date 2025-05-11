<div class="tcolorbox">

notions de bases des circuits, tension et intensité, conducteurs ohmiques, Lois de Kirchoff

</div>

# Rappels (du collège & de la seconde)

Nous allons commencer par quelques rappels des notions sur les circuits électriques que vous auriez du voir au collège. Il s’agit principalement de définitions.

## Dipôles électriques

Les dispositifs que l’on voit au collège et au lycée sont presque exclusivement des dipôles.

<table>
<caption>Un tableau récapitulatif des dipôles les plus fréquemment utilisés.</caption>
<thead>
<tr>
<th style="text-align: center;">Pile</th>
<th style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[battery1] (2,0);</p>
</div></th>
<th style="text-align: center;">Générateur</th>
<th style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[vsource] (2,0);</p>
</div></th>
<th style="text-align: center;">Interrupter</th>
<th style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[normal open switch] (2,0);</p>
</div></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;">Voltmètre</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) – (0.5,0) ; (1,0) circle (0.5cm) node <span>V</span>;(1.5,0) – (2,0);</p>
</div></td>
<td style="text-align: center;">Résistance</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[generic] (2,0);</p>
</div></td>
<td style="text-align: center;">Lampe</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[lamp] (2,0);</p>
</div></td>
</tr>
<tr>
<td style="text-align: center;">Ampèremètre</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,-1) – (0.5,-1) ; (1,-1) circle (0.5cm) node <span>A</span>;(1.5,-1) – (2,-1);</p>
</div></td>
<td style="text-align: center;">Diode</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[diode] (2,0);</p>
</div></td>
<td style="text-align: center;">DEL</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[led] (2,0);</p>
</div></td>
</tr>
<tr>
<td style="text-align: center;">Condensateur</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[capacitor] (2,0);</p>
</div></td>
<td style="text-align: center;">Bobine (inducteur)</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) to[cute inductor] (2,0);</p>
</div></td>
<td style="text-align: center;">Moteur</td>
<td style="text-align: center;"><div class="circuitikz">
<p>(0,0) – (0.5,0) ; (1,0) circle (0.5cm) node <span>M</span>;(1.5,0) – (2,0);</p>
</div></td>
</tr>
</tbody>
</table>

<div class="leftbar">

**Définition : *Dipôle électrique***

- Un **dipôle** est un composant électrique avec une entrée de courant et une sortie, d’où l’appellation *di*pôle.

- Les dipôles tombent en deux catégories : générateur ou récepteur<span style="color: purple">(= electrical load</span>)

  - **Générateur** : Un dipôle qui **fournit l’énergie électrique** au circuit. Il le fait en convertissant une forme d’énergie en énergie électrique (générant ainsi une tension électrique entre ses bornes), et ce qui permet le courant électrique de circuler dans le circuit.

  - **Récepteur** : Un dipôle qui effectue un ’action’ grâce au courant électrique qui le traverse. Autrement dit, qui **convertit l’énergie électrique du circuit en une autre forme d’énergie**.

</div>

## Intensité du courant & Tension électrique

<div class="multicols">

2

<div class="leftbar">

**Définition : *Tension électrique***

- La tension électrique $`U`$ , est la **différence de potentiel électrique** $`V_A`$ et $`V_B`$ entre deux points différents (du circuit) :
  ``` math
  U_{AB} = V_B - V_A
  ```

- La tension s’exprime en $`Volts\; V`$.

- La tension électrique entre deux points d’un circuit se mesure grâce à un *voltmètre*.

- Un voltmètre est branché **en dérivation** par rapport aux deux points. Si branché en série, il se comporte comme un interrupteur ouvert.

</div>

<div class="leftbar">

**Définition : *Intensité du courant***

- L’intensité du courant, noté $`I`$ ou $`i`$, est une mesure de la **quantité de charge électrique (notée $`Q`$ ou $`q`$) qui passe devant un point du circuit en une seconde** : $`I = \nicefrac{Q}{\Delta t}`$

- Le débit/intensité instantané est donné par :
  ``` math
  i(t) = \od{q}{t}
  ```

- L’intensité du courant s’exprime en *ampère* $`A=C\cdot s^{-1}`$.

- L’intensité se mesure grâce à un *ampèremètre*<span style="color: purple">(= ammeter</span>).

- Un ampèremètre est branché **en série** dans un circuit. Si branché en dérivation, cela fera un court-circuit.

</div>

</div>

<div class="wrapfigure">

r0.4 <img src="imgs/p7/analogie.jpg" style="width:85.0%" alt="image" />

</div>

<div class="mdframed">

**Remarque.** *Tandis que l’intensité du courant est une notion facile à comprendre et à visualiser, la notion de tension électrique est plus difficile à saisir, à première vue. D’une part, une analogie simple qui permet de mieux voir l’intensité du courant serait de compter le nombre de personnes qui passent devant un point pendant une période: plus il y a de personnes qui passe, plus le *courant* est intense (ici les *personnes* sont l’équivalent des électrons, par exemple, ou plus généralement de la charge électrique).*

D’autre part la tension électrique est aux différence de potentiels gravitationnels. Si nous mettons un ballons sur une terre plate, il ne bougerait pas. Si on le met sur une légère pente, il commence à rouler doucement vers le bas. Ceci est du à la différence de potentiel gravitationnel, car la position de départ et de la fin ne sont pas à la même hauteur, autrement dit aux différents potentiels gravitationnels. Plus cette différence est importante, plus le ballon roule avec une vitesse importante, et plus il peut surmonter, par exemple, les obstacles sur son chemin. La situation est quasi-identique avec une particule chargée dans un champ électrique. La tension générée par un pile par exemple est la différence de potentiel électrique entre sa sortie et son entrée. C’est cette différence qui donne l’impulsion aux particules chargées pour se déplacer dans le circuit.

</div>

## Circuit électrique

Un circuit électrique est un ensemble de conducteurs et de dispositifs électriques, reliés entre eux par des fils électriques. Un circuit comporte, presque toujours, un ou plusieurs générateur qui est la source de l’énergie électrique qui circule dans le circuits, et d’un ou plusieurs récepteur qui reçoivent cette énergie électrique afin de le convertir en une autre forme d’énergie (mécanique, ou thermique par exemple.

### Le sens du courant

Un courant électrique est la manifestation des charges électriques qui se déplace. Dans un solide ces charges sont des électrons qui se déplacent dans le matériau conducteur (dans ce qu’on appelle la bande de conduction). Mais dans un liquide (ou solution) ce sont des particules chargées, autres qu’électrons, qui sont responsable pour le courant électrique, des ions par exemple.

Les caractéristiques du courant, son sens et son intensité sont imposés par le générateur. **A l’extérieure d’un générateur, le courant électrique va de la borne $`+`$ vers la borne $`-`$ du générateur**.

<div class="center">

<div class="circuitikz">

(0,0) to\[battery1,\*-\*, v\<=$`U`$, i\<=$``$\] (3,0) ; (0.9,0.3) node$`+`$; (2.1,0.3) node$`-`$;

</div>

<div class="circuitikz">

(0,0) to\[vsource,\*-\*, v\<=$`U`$, i\<=$``$\] (3,0) ; (0.9,0.3) node$`+`$; (2.1,0.3) node$`-`$;

</div>

</div>

<div class="mdframed">

**Remarque.** *Nous savons que le courant est dû au mouvement des électrons dans les fils. Or les électrons, négativement chargés, vont vers le pôle $`+`$ du générateur. Cela veut dire que le sens de circulation des électrons est de $`-`$ vers $`+`$, c’est à dire le sens opposé au mouvement!*

La raison est plutôt historique : l’étude de l’électricité et de ses propriétés date du $`XVIII^e`$ siècle, alors que l’électron n’a été découvert qu’en 1897 (par J.J.Thompson). Toute la description des courants électriques été basée donc sur l’idée que les porteurs de charges étaient positivement chargés. Ce qu’on appelle aujourd’hui des *trous*.

</div>

### Branchement en série & en dérivation

<figure>
<div class="circuitikz">
<p>(0,4) to[short, i=<span class="math inline"><em>i</em></span>] (2,4) to [R, i=<span class="math inline"><em>i</em><sub>1</sub></span>, l=<span class="math inline"><em>R</em><sub>1</sub></span>] (2,0) ; (2,4) – (4,4) to[R, l=<span class="math inline"><em>R</em><sub>2</sub></span>, i=<span class="math inline"><em>i</em><sub>2</sub></span>] (4,0) – (0,0) ; (2,4) circle (1pt) ; (2,0) circle (1pt) ; (0,4) circle (1pt) ; (0,0) circle (1pt) ;</p>
</div>
<div class="circuitikz">
<p>(0,4) to[short, i=<span class="math inline"><em>i</em></span>] (2,4) to[R, i=<span class="math inline"></span>, l=<span class="math inline"><em>R</em><sub>1</sub></span>] (2,2) to[R, l=<span class="math inline"><em>R</em><sub>2</sub></span>] (2,0) to[short, i=<span class="math inline"></span>] (0,0) ; (0,4) circle (1pt) ; (0,0) circle (1pt) ;</p>
</div>
<figcaption>Branchement en dérivation à gauche, en série à droite</figcaption>
</figure>

### Conventions récepteur & générateur

Comme nous l’avons déjà mentionné, un générateur fournit l’énergie électrique au circuit, tandis que les récepteur la consomme, ou convertissent en une autre forme. Ceci se manifeste en une variation du potentiel électrique opposée entre les récepteurs et les générateurs. Autrement dit un générateur augment la différence de potentiel électrique, et un récepteur diminue le potentiel électrique. La tension entre les bornes d’une générateur n’a pas le même signe que la tension entre les bornes d’un récepteur, comme on va voir.

<div class="wrapfigure">

r0.4

<div class="circuitikz">

(0,0) to\[lamp,\*-\*, i\<=$``$, v^=$`U_R`$\] (3,0) ;

</div>

<div class="circuitikz">

(0,0) to\[battery1,\*-\*, v\<=$`U`$, i\<=$``$\] (3,0) ; (0.9,0.3) node$`+`$; (2.1,0.3) node$`-`$;

</div>

</div>

Dans représentation symbolique des diagrammes de circuit, ceci est est traduit par le sens de la flèche indiquant la tension du dipôle. Nous parlons alors de la convention générateur, et convention récepteur.

- **Convention générateur** : le sens de la flèche de la tension est le même que celui du courant.

- **Convention récepteur** : le sens de la flèche de la tension est opposé au celui du courant.

<div class="shaded">

**Exemple:**

<div class="wrapfigure">

r0.35

<div class="center">

<div class="circuitikz">

(0,3) to\[battery1, i=$`i`$\] (0,0); (0,3) – (3,3) to\[lamp, i=$`i`$\](3,0) – (0,0); (1.5,3) circle \[radius=0.05\]; (1.5,0) circle \[radius=0.05\]; (1.5,0.2) – (1.5,2.8); at (1.5,1.5) $`U`$;

</div>

</div>

</div>

Considérons le circuit très simple ci-contre. Il s’agit d’un générateur et un récepteur, ici une lampe.

La tension entre deux points d’un circuit est toujours la même $`U`$. On voit donc que du point de vu du générateur cette tension est dans le même sens que le courant, tandis que pour le récepteur cette tension va au sens opposé au courant. Voici donc les conventions générateur et récepteur.

</div>

## Les Lois de Kirchoff

Nous avons vu au collège qu’il existe principalement deux types de circuits : **en série** (avec une seule boucle, ou **une seule maille**), et **en dérivation** (avec **plusieurs boucles ou mailles**).

Les lois qui nous disent comment la tension et l’intensité du courant se comportent dans des différents types de circuits, s’appellent les lois de Kirchoff <span style="color: purple">(= Kirchoff’s circuit laws</span>), d’après l’allemand Gustav Kirchoff :

- **$`1^{ère}`$ loi de Kirchoff** : Loi des mailles, concernant la division de la tension dans une maille.

- **$`2^{ème}`$ loi de Kirchoff** : Loi des noeuds, concernant la division du courant dans un noeud.

## Loi des Mailles

<div class="shaded">

**Dans chaque maille d’un circuit, la somme algébrique des tensions de tous les dipôles de la maille est toujours zéro.**

</div>

<div class="wrapfigure">

r0.4

<div class="center">

<div class="circuitikz">

(0,4) to\[V, v\<=$`U_G`$, i\<=$`i`$\] (0,0) ; (0,4) –(1,4) to \[R, l^=$`R_1`$, v\<=$`U_1`$, i=$`i`$\] (3,4) – (4,4) – (4,3) to\[R, l^=$`R_2`$, v\<=$`U_2`$\](4,1) – (4,0) – (3,0) to \[R, l^=$`R_3`$, v\<=$`U_3`$\] (1,0) – (0,0);

</div>

</div>

</div>

Dans le circuit ci-contre, d’après la loi des mailles on doit avoir la somme de toutes les tensions égale à $`0`$. Mais d’après la convention générateur, comme nous voyons sur le schéma le sens de la tension $`U_G`$ est opposé aux autres tension, et donc on en arrive à la relation :
``` math
\begin{aligned}
    0 &=-U_G + U_1 + U_2 + U_3  \\
    U_G &= U_1 + U_2 + U_3
\end{aligned}
```

Si l’on voulait interpréter le sens de cette relation, ou de la loi des mailles, on peut tout simplement dire que la tension générée par le générateur est égale à la somme des tension utilisée par les récepteur. Autrement, l’énergie consommée par l’ensemble des récepteurs est égale à l’énergie fournie par l’ensemble des générateurs.

## Loi des Noeuds

<div class="shaded">

**Dans chaque noeud d’un circuit électrique, la somme algébriques des intensités du courant entrant et sortant du noeud, est toujours nulle.**

</div>

<div class="wrapfigure">

r0.2 <img src="imgs/p7/noeud.png" style="width:90.0%" alt="image" />

</div>

Dans la figure ci-contre on voit un noeud quelconque dans un circuit. On voit clairement qu’il y a deux courant qui entrent dans le noeud, et deux qui sortent. D’après la loi des noeuds donc, la somme de ces quatre intensités doit être nulle.

Mais il faut respecter le signe algébrique de chaque courant, c’est à dire quand le courant entre $`i>0`$, et quand le courant sort $`i<0`$. La relation mathématique relevant de la loi des noeuds est donc :
``` math
\begin{aligned}
    i_1 + i_2 - i_3 - i_4 &= 0 \\
    i_1 + i_2 &= i_3 - i_4
\end{aligned}
```

Ce résultats, et la loi des noeuds, est plutôt facile à interpréter. L’intensité du courant est une mesure du débit de charge électrique. Dans ce cas-là dit simplement qu’autant de charge sort d’un noeud, qui y entre, et l’inverse.

<div class="mdframed">

**Remarque.** *Les deux lois de Kirchoff sont les manifestations de deux principes fondamentaux et importants de la physique. La loi des mailles est une conséquence du principe de la **conservation de l’énergie**, et la loi des noeuds est une conséquence du principe de la **conservation de la charge électrique**.*

</div>

## Le conducteur ohmique

Une des manières la plus courante d’étudier le comportement d’un dipôle électrique, est grâce à sa **courbe caractéristique** <span style="color: purple">(= current-voltage characteristic</span>) (parfois appelé simplement sa *caractéristique*).

Il s’agit d’un graphique qui montre l’évolution de la tension $`U`$ entre les bornes du dipôle en fonction de $`I`$, l’intensité du courant qui le parcourt (i.e. le graphique $`U=f(I)`$). Dans certains livre la caractéristique peut être donnée comme $`I=f(U)`$. Cela n’est qu’un changement de représentation, et ne change pas le fond de ce que la caractéristique révèle.

### Conducteur Ohmique

<div class="wrapfigure">

r0.25 <img src="imgs/p7/car1.jpg" style="width:95.0%" alt="image" />

</div>

Vous connaissez déjà le conducteur ohmique depuis la classe de quatrième. C’est le dipôle récepteur le plus simple que vous avez rencontré, avec le symbole

<div class="circuitikz">

(0,0) to\[ R \] (2,0);

</div>

.

Le conducteur ohmique est la catégorie des dipôles ayant un comportement caractérisé par la courbe caractéristique ci-contre. Autrement dit, tous dipôles ayant une tension qui varie de manière linéaire en fonction de l’intensité du courant.

### La loi d’Ohm

La variation de $`U`$ en foncions de $`I`$ étant linéaire, on peut le modéliser mathématiquement par une fonction du type $`y = m\cdot x`$, où $`m`$ est le coefficient directeur du graphique précédent, c’est à dire la constante de proportionnalité entre la tension $`U`$ et l’intensité $`I`$. Dans notre modélisation donc l’ordonnée $`y`$ correspond à la tension $`U`$, et l’abscisse $`x`$ correspond à l’intensité $`I`$, ce qui donne une loi que vous connaissez déjà : La loi d’Ohm.

Avec $`R`$ comme constante de proportionnalité.

<div class="leftbar">

**Définition : *Loi d’Ohm***

- La loi d’Ohm est une loi empirique liant l’intensité du courant traversant un conducteur ohmique, et la tension entre ses bornes.

- Elle s’exprime mathématiquement :
  ``` math
  U = R\cdot I
  ```

- La constante de proportionnalité $`R`$ s’appelle la résistance du conducteur ohmique, et est une mesure, justement, de la résistance à l’intérieur du conducteur, au passage du courant électrique.

- $`R`$ s’exprime en *ohm*, noté par le symbole $`\ohm`$ (omega majuscule).

</div>

### Le générateur

<div class="wrapfigure">

l0.5 <img src="imgs/p7/car2.jpg" style="width:95.0%" alt="image" />

</div>

Nous n’allons pas entrer trop en détails cette année des différents types de générateur que l’on peut avoir (e.g. générateur de tension idéal, générateur de courant idéal, etc.), mais l’essentiel ne change pas : un générateur doit fournir l’énergie électrique au circuit, et est caractérisé par une tension qui doit rester plus ou moins constante et stable.

Nous faisons la distinction entre un générateur **idéal** et un générateur **réel**. C’est d’ailleurs une distinction que nous faisons souvent. La **différence entre un dipôle réel et idéal est la présence d’une petite résistance interne**. Un dipôle idéal, est tel, car on suppose qu’il n’y a aucune résistance au passage du courant à son intérieur, tandis que dans le monde réel, tout dipôle possède une certaine résistance interne, même si elle peut être très faible.

Un générateur idéal arrive à maintenir la tension qu’il génère, alors qu’un générateur réel, perd une partie de l’énergie qu’elle produise en raison de cette résistance interne. La tension générée par un générateur réel, selon la courbe caractéristique ci-contre est de forme :

``` math
U = U_G - r\cdot I \quad \quad
\begin{cases}
r \text{ est la résistance interne du générateur}\\
U \text{ est la tension réelle fournie par le générateur}\\
U_G \text{ est la tension idéale (nominale) du générateur}\\
I \text{ est l'intensité du courant qui parcourt le générateur}
\end{cases}
```

### Le point de fonctionnement

Nous pouvons maintenant utiliser toutes les informations précédente afin de déterminer dans quel étant fonctionnerait notre circuit. Étant donné que dans un circuit simple (caractérisé par les courbes ci-contre), il faut la même tension électrique et intensité du courant dans le générateur que dans le dipôle ohmique y branché, le circuit fonctionnerait à l’intersection des deux caractéristiques. Ce point est nommé le **point de fonctionnement**. L’intensité du fonctionnement $`I_f`$ est donc l’intensité du courant qui circulerait dans le circuit, et la tension du fonctionnement $`U_f`$ serait la tensions entre les bornes du générateur et du récepteur.

<figure>

<figcaption>Détermination graphique du point de fonctionnement.</figcaption>
</figure>

Cette analyse est parfaitement valable pour des circuits encore plus compliqué, comportant par exemple plusieurs conducteurs ohmiques.

# Le dipôle Condensateur

En électronique il y a trois dipôles principaux que l’on étudie : la résistance (conducteur ohmique), le condensateur, et la bobine d’induction (inducteur). Il y a, bien sur, d’autres dipôles aussi, mais ces trois-là ont un comportement particulier chacun qui nous permet d’analyser de manière complète le comportement des circuits électroniques.

## Principe de fonctionnement

<div class="leftbar">

**Définition : *Condensateur<span style="color: purple">(= capacitor</span>)***

- Un condensateur est un dipôle électronique composé de deux surface conductrices, appelées des **armatures**, séparées d’une distance.

- Les armatures sont souvent plates et parallèles, séparées d’un isolant, souvent l’air.

- Le symbole universel du condensateur est

  <div class="circuitikz">

  (0,0) to\[ C \] (2,0);

  </div>

  .

- Le condensateur est caractérisé par sa capacité $`C`$, qui s’exprime en $`Farads\; (F)`$.

</div>

Lorsqu’on applique une tension aux borne du condensateur, il y a une accumulation de charge $`Q`$ qui commence sur les armatures. Ceci est du à la présence de l’isolant entre ces deux dernières. La capacité $`C`$ d’un condensateur dépend de divers facteurs : la superficie des armatures, leur matériau, la distance entre elles, la nature de l’isolant, etc. **On peut considérer le condensateur donc comme un dipôle “stockeur” de charge.**

Le fonctionnement, et le comportement d’un condensateur est en raison de l’accumulation de la charge sur ses armatures (phase de charge), et la décharge de ses armatures (phase de décharge), où il perds la charge accumulée. La **charge accumulée créé une tension entre les bornes du condensateur**, contre la tension imposée par le générateur.

## Caractéristiques du condensateur

La tension $`u_C`$ du générateur est donc proportionnelle à la charge accumulée $`q`$, et la capacité $`C`$ du condensateur:
``` math
u_C = \dfrac{q}{C} \quad \Longleftrightarrow \quad q=C\cdot u_C
```

La charge sur chaque armature est donc : $`q^+ = C\cdot u_C`$ et $`q^- = -C\cdot u_C`$.

<figure>
<figure>
<img src="imgs/p7/condensateur.jpg" />
</figure>
<figure>
<div class="center">
<div class="circuitikz">
<p>(0,3) to[V, i=<span class="math inline"><em>i</em></span>] (0,0); (0,3) – (3,3) to[C, i=<span class="math inline"><em>i</em></span>](3,0) – (0,0); (1.5,3) circle [radius=0.05]; (1.5,0) circle [radius=0.05]; (1.5,0.2) – (1.5,2.8); at (1.5,1.5) <span><span class="math inline"><em>U</em><sub><em>C</em></sub></span></span>;</p>
</div>
</div>
</figure>
<figcaption></figcaption>
</figure>

Nous avons alors tout ce qu’il nous faut pour établir une relation entre l’intensité (instantanée) du courant et la tension entre les bornes du condensateur :

``` math
\begin{aligned}
    i &= \od{q}{t} = \od{\left(C\cdot u_C\right)}{t} \\
    i &=C\od{u_C}{t}
\end{aligned}
```

# Le circuit RC

Un circuit contenant un conducteur ohmique $`R`$ et un condensateur $`C`$ s’appelle un circuit RC (quelle originalité, je sais). Ces dipôles peuvent être branchés en série ou en dérivation. Pour commencer nous nous intéressons aux cas les plus simples : le circuit RC en série.

## Régime transitoire & régime permanent

La conducteur ohmique est un dipôle qui réagit de manière instantanée et proportionnelle à l’intensité du courant qui le parcourt. Avec l’inclusion du condensateur la réponse du système est plus “lente” dans ses réactions, c’est à dire qu’il faut un temps pour que les tensions et les intensités se stabilisent.

On fait donc la différence entre le **régime permanent** (ou continu, ou stationnaire) où les tensions et les intensité dans les branches du circuits et dans les dipôles se sont stabilisées (des valeurs constantes), et le **régime variable ou transitoire** où les tensions et les intensité dans le circuit sont en cours de variation afin d’atteindre leurs valeurs stables en régime permanent.

<figure>
<img src="imgs/p7/regimes.jpg" style="width:80.0%" />
</figure>

Considérons le circuit électrique ci-après (cf Figure.<a href="#fig:decharge" data-reference-type="ref" data-reference="fig:decharge">1</a>). Nous allons donc étudier le comportement d’un condensateur en deux états : l’état de **charge**, et l’état de **décharge**.

<figure id="fig:decharge">
<figure>
<img src="imgs/p7/RCcharge.jpg" />
</figure>
<figure>
<img src="imgs/p7/RCdecharge.jpg" />
</figure>
<figcaption>Un circuit RC en deux modes : charge &amp; décharge</figcaption>
</figure>

Notre objectif principal dans les deux cas est d’obtenir l’équation (différentielle) du circuit, dont la solution nous permet de modéliser l’évolution de la tension (ou de la charge électrique) dans le circuit.

## Circuit de charge

<div class="wrapfigure">

r0.38 <img src="imgs/p7/RCcharge.jpg" alt="image" />

</div>

Le circuit RC est en charge (ou simplement le condensateur est en charge) lorsqu’il est branché sur le générateur. Dans ce cas de figure le **condensateur est un récepteur** (convention récepteur donc à respecter pour les tensions et les courants).

Afin d’obtenir l’équation différentielle du circuit **nous appliquons simplement la loi des mailles** à toutes les mailles concernées. Nous allons trouver l’équation différentielle du circuit en termes de $`u_C`$, mais aussi en termes de $`q`$, car les deux sont liées.

D’après la loi des mailles :

``` math
\begin{aligned}
    E - u_C - u_R &= 0 \\
    u_C + u_R &= E \\
    u_C + Ri &= E
\end{aligned}
```

<div class="multicols">

2 Pour trouver l’équation du système en termes de $`u_C`$ substituons avec $`(3)`$ :
``` math
u_C + RC\od{u_C}{t} = E
```

Mettons cette équation en sa forme canonique :
``` math
\od{u_C}{t} + \frac{1}{RC}u_C = \frac{E}{RC}
```

Pour trouver l’équation du système en termes de $`q`$ substituons avec $`(1)`$ et $`(2)`$ :

Mettons cette équation en forme canonique :
``` math
\vspace{1cm}
```

</div>

  
Nous appelons le produit $`RC`$, la **constante du temps** $`\tau = RC`$; et nous avons donc:
``` math
\begin{aligned}
    \od{u_C}{t} + \frac{1}{\tau}u_C &= \frac{E}{\tau} \\
    \od{q}{t} + \frac{1}{\tau}q &= \frac{E}{R}
\end{aligned}
```
Les solutions aux équations (6) et (7) sont :
``` math
\begin{aligned}
    u_C(t) &= E\left( 1 - e^{-\nicefrac{t}{\tau}}\right) \\
    q(t) &= 
\end{aligned}
```

<div class="shaded">

$`\triangleright \quad`$**Exercice .** A l’aide d’une analyse dimensionnelle justifier l’appellation “constante du temps” pour la constante $`\tau`$ .

</div>

<div class="shaded">

$`\triangleright \quad`$**Exercice .** Donner la solution générale aux équations (6) et (7), et puis démontrer comment nous obtenons les solutions (8) et (9). Expliciter vos raisonnements et suppositions.

</div>

Visualisons l’évolution de la tension $`u_C(t)`$ entre les bornes du condensateur (et donc dans le circuit, car il s’agit d’un circuit en série).

<figure>
<img src="imgs/p7/courbeCharge.jpg" style="width:70.0%" />
</figure>

La charge $`q(t)`$ évolue de la même manière (même fonction), avec la seule différence étant la valeur de l’asymptote qui correspond bien à $`CE`$.

<div class="shaded">

$`\triangleright \quad`$**Exercice .** Comment évolue l’intensité du courant $`i(t)`$? Montrer grâce à un calcul. Montrez le graphique de $`i(t)`$.

</div>

## Circuit de décharge

Comme nous avons vu dans la partie précédente, un condensateur se trouve soit dans un des deux états :

- Tant que le condensateur est branché sur un générateur, la tension $`u_c`$ et le condensateur accumule de la charge : il est en phase de charge. En mode charge, le condensateur est un récepteur.

- En absence de la tension imposée par un générateur, la charge accumulée par le condensateur commence à dissiper, et repartant dans le circuit la tension $`u_c`$ commence à diminuer : c’est la phase de décharge. En mode décharge le condensateur se comporte comme un **générateur**.

<figure>
<figure>
<img src="imgs/p7/RCdecharge.jpg" />
</figure>
<figure>
<img src="imgs/p7/rcDecharg2.jpg" />
</figure>
<figcaption>Décharge d’un condensateur dans une résistance.</figcaption>
</figure>

En appliquant la même méthodologie que dans la partie précédente nous trouvons les équations suivantes pour $`u_C(t)`$ et $`q(t)`$:
``` math
\begin{aligned}
    \od{u_C}{t} + \frac{1}{\tau}u_C &= 0 \\
    \od{q}{t} + \frac{1}{\tau}q &= 0
\end{aligned}
```
et leurs solutions :
``` math
\begin{aligned}
    u_C(t) &= E\cdot e^{-\nicefrac{t}{\tau}} \\
    q(t) &= CE\cdot e^{-\nicefrac{t}{\tau}}
\end{aligned}
```

Voici comment la tension $`u_C(t)`$ évolue avec le temps :

<figure>
<img src="imgs/p7/courbeDecharge.png.jpg" style="width:70.0%" />
</figure>

<div class="shaded">

$`\triangleright \quad`$**Exercice .** Faire la démonstration pour obtenir les équations (10) et (11), avec $`\tau = RC`$. Montrer comment nous obtenons les solutions (12) et (13).

</div>

## Détermination du $`\tau`$

Il existe différentes manières de déterminer la valeur de la constante du temps $`\tau`$ graphiquement. Voici en quelques unes :

- Quand $`t=\tau`$ alors $`u_c(\tau) = E\left(1-e^{-1}\right) = 0,63E`$. En repérant l’abscisse correspondant à l’ordonnée $`0,63E`$, et cela correspondrait à $`\tau`$.

- Dans le cas d’une courbe de décharge, $`u_c(\tau) = E\cdot e^{-1} = 0,37E`$.

- Une autre propriété de la fonction exponentielle est que la tangente à l’origine de la courbe ($`u_C(t)`$) coupe l’asymptote à l’abscisse $`t=\tau`$. Pour rappelle l’asymptote pour un condensateur en charge correspond à $`u_C = E`$, et pour un condensateur en décharge $`u_C = 0`$

<figure>
<figure>
<img src="imgs/p7/courbeRC.jpg" />
</figure>
<figure>
<img src="imgs/p7/courbeDecharge2.jpg" />
</figure>
</figure>

<div class="mdframed">

**Remarque.** *Une autre propriété de la fonction exponentielle (que nous avons déjà vu dans les autres chapitres où la fonction exponentielle est exploitée) est que au bout de $`t\approx5\tau`$ nous sommes passé en régime permanent.*

</div>

<div class="shaded">

$`\triangleright \quad`$**Exercice .** Montrer que $`t\approx5\tau`$ est une bonne approximation de la durée du régime transitoire.

</div>

## Influence des caractéristiques du circuit

Les deux facteurs qui influence la constante du temps, et par conséquent la durée de charge ou décharge sont - pas très étonnement - les valeurs de la résistance $`R`$ et de la capacité $`C`$. En variants ces valeurs nous pouvons changer la vitesse de charge/décharge du circuit (c.f. figure <a href="#fig:tempsresist" data-reference-type="ref" data-reference="fig:tempsresist">2</a>).

<figure id="fig:tempsresist">
<figure>
<img src="imgs/p7/Figure_1.png" />
</figure>
<figure>
<img src="imgs/p7/Figure_2.png" />
</figure>
<figcaption>L’influence de la variation de la résistance sur la durée de charge (gauche) et de la décharge (droite).</figcaption>
</figure>
