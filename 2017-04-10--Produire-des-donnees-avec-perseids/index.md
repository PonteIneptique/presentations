Produire des données en Sciences de l'Antiquité avec Perseids
===  

.subtitle[Comment et pour quoi faire ?]

.author[Thibault Clérice ( prénom\.nom\[at\]uni-leipzig.de )] 

.author[Github/Twitter : @ponteineptique] 

---

# Objectifs

- Présenter Perseids et les différents points qui font sa fondation
	1. Le Projet
	2. Publier
	3. API
	4. Standards
- Les outils de Perseids
	1. Transcription
	2. Plokamos et l'annotation de textes
	2. Arethusa & le treebank
- Utiliser les données de Perseids : des exemples
	1. Valorisation du Patrimoine
	2. Apprendre le latin et le grec à une machine
	3. Valeurs sémantiques
	4. Utilisations d'outils : attention !
- Conclusion

---

# Qu'est-ce que Perseids ?

## Administrativement

- financé par la A. W. Mellon Fundation
- monté à Tufts
- enfant/frère de la Perseus Digital Library
- dans sa deuxième phase (1ère phase de X ans, 2ème depuis octobre sur X ans)
- dirigé par Marie-Claire Beaulieu et Bridget Almas

## Ses objectifs

- Introduire dans les cours licence/master la notion de publication
- Arrêter d'abandonner les données de l'enseignement
- Aider des projets ou des chercheur.se.s à mettre en place leur recherche dans un ENT

???

Commencer par un rapide condensé de ce qu'est Perseids

---
## Comment fonctionne la publication d'un article universitaire

![http://thescipub.com/](images/thescipub-workflow.png)

Le processus de publication est complètement intégré à Perseids et est réutilisé par d'autres projets tels que Eagle-network.eu et Syriaca.org.

???

Ce système du publication est mis à disposition des chercheur-se-s, projets et étudiant-e-s entre autres pour favoriser la collaboration.

---
class: top
## API

- Application Programming Interface, Interface de Programmation 
- Utilisé par les machines pour communiquer avec des machines

???

Je parlerai souvent d'API dans le contexte de ma présentation aussi il me semble normal d'introduire ce concept en amont.

Une API, Application Programming Interface, permet à une machine de communiquer avec une autre machine. On ne parle bien sûr pas là de discours autonome au coin du disque dur. Il s'agit pour un-e chercheur-se de communiquer avec un service et d'en extraire l'information dont il a besoin pour faire sa recherche.

---
class: top

## API vs. Interface Utilisateur

[Homer, Odyssey, 9.1](http://www.perseus.tufts.edu/hopper/text?doc=Perseus%3Atext%3A1999.01.0135%3Abook%3D9%3Acard%3D1)

![https://libraryofantiquity.files.wordpress.com/2016/03/perseus1-text-location-search.png](images/perseus1-text-location-search.png)

???

Voici une interface utilisateur basique, connue de tous, quoiqu'un peu vieillie

---
class: top

## API vs. Interface Utilisateur

![http://www.perseus.tufts.edu/hopper/help/texts](images/texthelp1.png)

---
class: top

## API vs. Interface Utilisateur

![http://www.perseus.tufts.edu/hopper/help/texts](images/texthelp2.png)

---
class: top

## API vs. Interface Utilisateur (4)

[http://ctsstage.dh.uni-leipzig.de/api/cts?request=GetPassagePlus&urn=urn:cts:greekLit:tlg0012.tlg002.perseus-grc2:9.1-9.46](http://ctsstage.dh.uni-leipzig.de/api/cts?request=GetPassagePlus&urn=urn:cts:greekLit:tlg0012.tlg002.perseus-grc2:9.1-9.46)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<GetPassagePlus>
   <request>
      <requestName>GetPassagePlus</requestName>
      <requestUrn>urn:cts:greekLit:tlg0012.tlg002.perseus-grc2:9.1-9.46</requestUrn>
   </request>
   <reply>
      <urn>urn:cts:greekLit:tlg0012.tlg002.perseus-grc2:9.1-9.46</urn>
      <passage>
         <TEI>
            <text>
               <body>
                  <div type="edition" n="urn:cts:greekLit:tlg0012.tlg002.perseus-grc2" xml:lang="grc">
                     <div n="9" type="textpart" subtype="book">
                        <l n="1">τὸν δʼ ἀπαμειβόμενος προσέφη πολύμητις Ὀδυσσεύς·</l>
                        <q type="unspecified">
                           <l n="2">Ἀλκίνοε κρεῖον, πάντων ἀριδείκετε λαῶν,</l>
                           <l n="3">ἦ τοι μὲν τόδε καλὸν ἀκουέμεν ἐστὶν ἀοιδοῦ</l>
                           <l n="4">τοιοῦδʼ οἷος ὅδʼ ἐστί, θεοῖς ἐναλίγκιος αὐδήν.</l>
                           <l n="5">οὐ γὰρ ἐγώ γέ τί φημι τέλος χαριέστερον εἶναι</l>
                           <l n="6">ἢ ὅτʼ ἐυφροσύνη μὲν ἔχῃ κάτα δῆμον ἅπαντα,</l>
                           <l n="7">δαιτυμόνες δʼ ἀνὰ δώματʼ ἀκουάζωνται ἀοιδοῦ</l>
                           <l n="8">ἥμενοι ἑξείης, παρὰ δὲ πλήθωσι τράπεζαι</l>
                           <l n="9">σίτου καὶ κρειῶν, μέθυ δʼ ἐκ κρητῆρος ἀφύσσων</l>
                           <l n="10">οἰνοχόος φορέῃσι καὶ ἐγχείῃ δεπάεσσι·</l>
                           <l n="11">τοῦτό τί μοι κάλλιστον ἐνὶ φρεσὶν εἴδεται εἶναι.</l>
                           <l n="12">σοὶ δʼ ἐμὰ κήδεα θυμὸς ἐπετράπετο στονόεντα</l>
                           <l n="13">εἴρεσθʼ, ὄφρʼ ἔτι μᾶλλον ὀδυρόμενος στεναχίζω·</l>
                           <l n="14">τί πρῶτόν τοι ἔπειτα, τί δʼ ὑστάτιον καταλέξω;</l>
                           <l n="15">κήδεʼ ἐπεί μοι πολλὰ δόσαν θεοὶ Οὐρανίωνες.</l>
                           <l n="16">νῦν δʼ ὄνομα πρῶτον μυθήσομαι, ὄφρα καὶ ὑμεῖς</l>
                           <l n="17">εἴδετʼ, ἐγὼ δʼ ἂν ἔπειτα φυγὼν ὕπο νηλεὲς ἦμαρ</l>
                           <l n="18">ὑμῖν ξεῖνος ἔω καὶ ἀπόπροθι δώματα ναίων.</l>
                           <l n="19">εἴμʼ Ὀδυσεὺς Λαερτιάδης, ὃς πᾶσι δόλοισιν</l>
                           <l n="20">ἀνθρώποισι μέλω, καί μευ κλέος οὐρανὸν ἵκει.</l>
                           <l n="21">ναιετάω δʼ Ἰθάκην ἐυδείελον· ἐν δʼ ὄρος αὐτῇ</l>
                           <l n="22">Νήριτον εἰνοσίφυλλον, ἀριπρεπές· ἀμφὶ δὲ νῆσοι</l>
                           <l n="23">πολλαὶ ναιετάουσι μάλα σχεδὸν ἀλλήλῃσι,</l>
                           <l n="24">Δουλίχιόν τε Σάμη τε καὶ ὑλήεσσα Ζάκυνθος.</l>
                           <l n="25">αὐτὴ δὲ χθαμαλὴ πανυπερτάτη εἰν ἁλὶ κεῖται</l>
                           <l n="26">πρὸς ζόφον, αἱ δέ τʼ ἄνευθε πρὸς ἠῶ τʼ ἠέλιόν τε,</l>
                           <l n="27">τρηχεῖʼ, ἀλλʼ ἀγαθὴ κουροτρόφος· οὔ τοι ἐγώ γε</l>
                           <l n="28">ἧς γαίης δύναμαι γλυκερώτερον ἄλλο ἰδέσθαι.</l>
                           <l n="29">ἦ μέν μʼ αὐτόθʼ ἔρυκε Καλυψώ, δῖα θεάων,</l>
                           <l n="30">ἐν σπέσσι γλαφυροῖσι, λιλαιομένη πόσιν εἶναι·</l>
                           <l n="31">ὣς δʼ αὔτως Κίρκη κατερήτυεν ἐν μεγάροισιν</l>
                           <l n="32">Αἰαίη δολόεσσα, λιλαιομένη πόσιν εἶναι·</l>
                           <l n="33">ἀλλʼ ἐμὸν οὔ ποτε θυμὸν ἐνὶ στήθεσσιν ἔπειθον.</l>
                           <l n="34">ὣς οὐδὲν γλύκιον ἧς πατρίδος οὐδὲ τοκήων</l>
                           <l n="35">γίγνεται, εἴ περ καί τις ἀπόπροθι πίονα οἶκον</l>
                           <l n="36">γαίῃ ἐν ἀλλοδαπῇ ναίει ἀπάνευθε τοκήων.</l>
                           <l n="37">εἰ δʼ ἄγε τοι καὶ νόστον ἐμὸν πολυκηδέʼ ἐνίσπω,</l>
                           <l n="38">ὅν μοι Ζεὺς ἐφέηκεν ἀπὸ Τροίηθεν ἰόντι.</l>
                           <l n="39">
                              <milestone unit="para" ed="P" />
                              Ἰλιόθεν με φέρων ἄνεμος Κικόνεσσι πέλασσεν,
                           </l>
                           <l n="40">Ἰσμάρῳ. ἔνθα δʼ ἐγὼ πόλιν ἔπραθον, ὤλεσα δʼ αὐτούς·</l>
                           <l n="41">ἐκ πόλιος δʼ ἀλόχους καὶ κτήματα πολλὰ λαβόντες</l>
                           <l n="42">δασσάμεθʼ, ὡς μή τίς μοι ἀτεμβόμενος κίοι ἴσης.</l>
                           <l n="43">ἔνθʼ ἦ τοι μὲν ἐγὼ διερῷ ποδὶ φευγέμεν ἡμέας</l>
                           <l n="44">ἠνώγεα, τοὶ δὲ μέγα νήπιοι οὐκ ἐπίθοντο.</l>
                           <l n="45">ἔνθα δὲ πολλὸν μὲν μέθυ πίνετο, πολλὰ δὲ μῆλα</l>
                           <l n="46">ἔσφαζον παρὰ θῖνα καὶ εἰλίποδας ἕλικας βοῦς·</l>
                        </q>
                     </div>
                  </div>
               </body>
            </text>
         </TEI>
      </passage>
      <prevnext>
         <prev>
            <urn>8.541-8.586</urn>
         </prev>
         <next>
            <urn>9.47-9.92</urn>
         </next>
      </prevnext>
      <label>
         <groupname xml:lang="eng">Homer</groupname>
         <title xml:lang="eng">Odyssey</title>
         <label xml:lang="eng">Odyssey, Loeb classical library</label>
         <description xml:lang="eng">Homer, creator; Murray, A. T. (Augustus Taber), 1866-1940, editor</description>
         <citation label="book" xpath="/tei:div[@n='?']" scope="/tei:TEI/tei:text/tei:body/tei:div">
            <citation label="line" xpath="//tei:l[@n='?']" scope="/tei:TEI/tei:text/tei:body/tei:div/tei:div[@n='?']" />
         </citation>
      </label>
   </reply>
</GetPassagePlus>


```

---
## Les standards

Les standards concernent différents aspects des données : leur forme et leur mode d'accès.

On dénombre dans le monde des sciences de l'antiquités plusieurs standards d'API intéressants :
- CTS (Canonical Text Services) pour partager et accéder aux textes
- IIIF (International Image Interoperability Framework) pour partager des images
- API liées aux SIG ?
- Sparql : interroger des bases de données de manière standard (Quel âge avait Seneque quand il est mort ?)

Et quelques formats :
- TEI ou Epidoc pour partager des contenus textuels
- GEOJson polur partager des données géographiques
- RDF (Turtle, XML, N3, etc.)

---

Les outils de Perseids
======================

1. Publier
2. Annoter
3. Analyser

---

Publier [1]
===========

## Status
- Limité à la publication basée sur les textes disponibles
- Objectif d'ouvrir pour publier selon les normes CapiTainS (Quelque soit le type de texte et la langue !)
- Traduire et/ou éditer des inscriptions, des manuscrits

## Principal utilisation : 
- Enseignement

---

Publier [2]
===========

[Edition d'un Miscellany](http://sosol.perseids.org/sosol/publications/35125/epi_cts_identifiers/46932/editxml)

![](images/Perseids_epi_cts_identifiers_-_editxml_-_2017-04-10_16.31.06.png)

---

Publier [3]
===========

```xml

<div xml:lang="grc" type="edition" xml:space="preserve">
	<lg met="">
	<l n="1">
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.1888,0.0847,0.0720,0.0115">Raebuerat</w>
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.2625,0.0844,0.0360,0.0118">dictis</w>
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.3006,0.0930,0.0042,0.0036">.</w>
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.3041,0.0852,0.0742,0.0118">Certamina</w>
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.3802,0.0851,0.0483,0.0123">musarum</w>
		<w facs="urn:cite:perseus:miscellanyimgs.UWDkbqJfqQc@0.4327,0.0880,0.0304,0.0099">cum</w>
	</l>
</lg>
</div>
```