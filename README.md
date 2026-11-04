<!--
author:   Jan Vanvinkenroye
email:    jan.vanvinkenroye@tik.uni-stuttgart.de
version:  1.1.1
language: de
narrator: Deutsch Female
mode:     Textbook
logo:     img/eh-logo.svg

comment:  Selbstlerneinheit fuer Studierende der Sozialen Arbeit: den
          Medienkompetenzbegriff nach Dieter Baacke erarbeiten, an Faellen
          anwenden, kritisch einordnen und daraus eigene Lernziele und ein
          medienpaedagogisches Angebot entwickeln. Dauer ca. 150 Minuten.

link:     https://fonts.googleapis.com/css2?family=Barlow+Semi+Condensed:wght@300;400;500;600&display=swap

@style
/* Gestaltung nach dem Typst-Template ehlb-handout (EH Ludwigsburg):
   EH-Gruen #098C49, Dunkelgruen #054926, Gruen-Tints, Textgrau #575756,
   Barlow Semi Condensed als freier Ersatz fuer GT Walsheim Pro Condensed. */
:root, :root.lia-theme-default {
  --color-highlight:      9, 140, 73;
  --color-highlight-dark: 5, 73, 38;
  --color-highlight-menu: 9, 140, 73;
  --color-accent:         rgb(9, 140, 73);
  --global-font-family:   "Barlow Semi Condensed", "Barlow", Arial, sans-serif;
  --global-font-headline: "Barlow Semi Condensed", "Barlow", Arial, sans-serif;
  --eh-gruen:       #098C49;
  --eh-dunkelgruen: #054926;
  --eh-hellgruen:   #CEE8DB;
  --eh-mintgruen:   #BADFCC;
  --eh-grau:        #575756;
  --eh-anthrazit:   #212529;
  --eh-linie:       #DEE2E6;
}
:root.lia-variant-light { --color-text: 87, 87, 86; }

h1, h2, h3, h4, h5, h6 {
  font-family: var(--global-font-headline) !important;
  font-weight: 500 !important;
  letter-spacing: 0;
}
/* Folientitel gruen wie der Handout-Titel, Zwischentitel dunkelgruen */
main h1, main h2 { color: var(--eh-gruen); }
main h3, main h4 { color: var(--eh-dunkelgruen); }
main ul > li::marker { color: var(--eh-gruen); }
main ol > li::marker { color: var(--eh-gruen); font-weight: 500; }
.lia-table .lia-table__header { background: var(--eh-hellgruen) !important; color: var(--eh-anthrazit); }
.lia-variant-dark .lia-table .lia-table__header { background: rgba(9, 140, 73, 0.3) !important; color: inherit; }
main strong, main b { font-weight: 500; }
main a { color: var(--eh-gruen); }

main blockquote {
  border-left: 3px solid var(--eh-gruen);
  background: rgba(206, 232, 219, 0.35);
  padding: 0.6rem 1rem;
}

/* ehlb-box: heller Infokasten mit gruenem Balken */
.box {
  border-left: 3px solid var(--eh-gruen);
  background: #DDEFE6;
  padding: 10px 12px;
  margin: 1em 0;
}
.box b:first-child { color: var(--eh-dunkelgruen); }
/* ehlb-wichtig: dunkelgruener Hinweis, weisse Schrift */
.box.warn { border-left: 0; background: var(--eh-dunkelgruen); color: white; }
.box.warn b:first-child, .box.warn b, .box.warn i { color: white; }
/* Merksatz: Mintgruen */
.box.ok { background: var(--eh-mintgruen); border-left-color: var(--eh-dunkelgruen); }
/* Arbeitsauftrag: weiss mit Linie */
.box.study { background: transparent; border: 1px solid var(--eh-linie); border-left: 3px solid var(--eh-gruen); }
.lia-variant-dark .box, .lia-variant-dark .box.ok { background: rgba(9, 140, 73, 0.18); color: inherit; }
.lia-variant-dark .box.study { background: transparent; }

/* ehlb-label: gruener Chip */
.dim {
  display: inline-block;
  background: var(--eh-gruen);
  color: white;
  font-weight: 500;
  padding: 5px 10px;
  margin: 0.2em 0 0.6em 0;
}

/* Kopf der Startseite wie Seite 1 des Handouts */
.eh-kopf {
  display: flex; justify-content: space-between; align-items: flex-start;
  gap: 1rem; flex-wrap: wrap;
  border-bottom: 1px solid var(--eh-linie); padding-bottom: 0.8rem; margin-bottom: 1rem;
}
.eh-kopf img { width: 150px; max-width: 45%; }
.eh-meta { text-align: right; font-size: 0.9em; color: var(--eh-grau); line-height: 1.4; }
.eh-untertitel { font-size: 1.25em; font-weight: 300; color: var(--eh-grau); margin-top: -0.4em; }
@end
-->

# Medienkompetenz nach Dieter Baacke

<div class="eh-untertitel">Selbstlerneinheit für Studierende der Sozialen Arbeit</div>

<div class="eh-kopf">
<img src="img/eh-logo.svg" alt="Logo der Evangelischen Hochschule Ludwigsburg">
<div class="eh-meta">
Selbstlerneinheit Medienpädagogik<br>
Jan Vanvinkenroye<br>
Ca. 150 Minuten
</div>
</div>


Medien sind aus der Lebenswelt der Adressat\*innen Sozialer Arbeit nicht wegzudenken: Gruppenchats im Jugendtreff, Videotelefonie mit Angehörigen im Pflegeheim, Online-Formulare beim Jobcenter, Desinformation im Familien-Chat. Fachkräfte der Sozialen Arbeit brauchen deshalb ein Modell, mit dem sie beschreiben können, *was* Menschen im Umgang mit Medien können sollten – und *wie* sich das fördern lässt.

Das einflussreichste Modell dafür im deutschsprachigen Raum stammt von **Dieter Baacke** (1934–1999).

<div class="box">
<b>Dein Arbeitsprodukt:</b> Am Ende dieser Einheit hast du die Skizze eines eigenen medienpädagogischen Angebots für eine Zielgruppe der Sozialen Arbeit – mit Lernzielen, die gezielt einzelne Dimensionen von Medienkompetenz fördern.
</div>

--{{0}}--
Willkommen zur Selbstlerneinheit Medienkompetenz nach Dieter Baacke. Du erarbeitest das Modell, wendest es an Fällen an und entwickelst am Ende ein eigenes Angebot.


## Orientierung

**Lernziele dieser Einheit** – nach der Bearbeitung kannst du …

1. die vier Dimensionen und acht Unterdimensionen von Medienkompetenz nach Baacke **benennen und erläutern**,
2. Medienkompetenz als Ausdifferenzierung **kommunikativer Kompetenz** einordnen,
3. Situationen aus der Praxis Sozialer Arbeit den Dimensionen **zuordnen**,
4. zentrale **Kritikpunkte** und Weiterentwicklungen des Modells wiedergeben,
5. **operationalisierte Lernziele** formulieren, die sich auf einzelne Dimensionen beziehen,
6. ein **medienpädagogisches Angebot** für eine Zielgruppe der Sozialen Arbeit skizzieren.

**Ablauf und Zeitbedarf**

| Abschnitt                          | Zeit       |
| :--------------------------------- | ---------: |
| 1 Einstieg: Mein Medienalltag      | ca. 10 Min. |
| 2 Woher kommt der Begriff?         | ca. 15 Min. |
| 3 Die vier Dimensionen             | ca. 30 Min. |
| 4 Anwendung: Fälle aus der Praxis  | ca. 20 Min. |
| 5 Kritik und Weiterentwicklungen   | ca. 15 Min. |
| 6 Lernziele formulieren            | ca. 20 Min. |
| 7 Eigenes Angebot entwickeln       | ca. 35 Min. |
| 8 Abschluss                        | ca. 5 Min. |
| **Gesamt**                         | **ca. 150 Min.** |

<div class="box warn">
<b>Wichtig zum Speichern:</b> Deine Eingaben in Textfeldern werden nur lokal in deinem Browser gespeichert. Kopiere deine Lernziele und deine Angebotsskizze (Abschnitt 6 und 7) zusätzlich in ein eigenes Dokument, wenn du sie behalten oder abgeben möchtest.
</div>


# 1 Einstieg: Mein Medienalltag

Bevor es um Theorie geht, ein Blick auf dich selbst und auf das Arbeitsfeld.

Welche Medien hast du heute schon genutzt – und wofür?

    [[___ ___ ___]]

Wo begegnen dir Medien in der Praxis der Sozialen Arbeit (Praktikum, Job, Ehrenamt)? Mehrfachauswahl möglich.

    [[Kommunikation mit Adressat*innen (Messenger, Mail)]]
    [[Konflikte oder Mobbing in sozialen Medien]]
    [[Digitale Antragsverfahren und Behördenkontakte]]
    [[Medienprojekte (Film, Foto, Podcast, Games)]]
    [[Fragen zu Datenschutz und Persönlichkeitsrechten]]
    [[Desinformation und Verschwörungserzählungen]]
    [[Bisher kaum]]

Wie schätzt du deine eigene Medienkompetenz ein?

- [(sehr hoch)]   sehr hoch
- [(eher hoch)]   eher hoch
- [(mittel)]      mittel
- [(eher gering)] eher gering

<div class="box study">
<b>Merke dir deine Antwort.</b> Am Ende der Einheit schaust du noch einmal darauf: Was genau meinst du eigentlich, wenn du "Medienkompetenz" sagst – Technik bedienen können? Kritisch sein? Selbst etwas produzieren?
</div>


# 2 Woher kommt der Begriff?

Baacke hat den Begriff Medienkompetenz nicht aus der Technik, sondern aus der **Kommunikationstheorie** entwickelt. Schon 1973 legte er mit *Kommunikation und Kompetenz* die Grundlage.

    {{1}}
<section>

**Medienkompetenz als Form kommunikativer Kompetenz**

Baacke versteht Medienkompetenz als „systemische Ausdifferenzierung von kommunikativer Kompetenz“ (Hugger 2022, S. 68, mit Bezug auf Baacke 1973, 1996). Der Grund: Unsere Kommunikation verändert sich ständig durch „technisch-industrielle Vorkehrungen und Erweiterungen“ (Baacke 1996, S. 119), in denen wir uns auch mit Medien ausdrücken (müssen).

Seine Kurzdefinition:

> Medienkompetenz meint „grundlegend nichts anderes als die Fähigkeit, in die Welt aktiv aneignender Weise auch alle Arten von Medien für das Kommunikations- und Handlungsrepertoire von Menschen einzusetzen.“ (Baacke 1996, S. 119)

</section>

    {{2}}
<section>

**Kompetenz und Performanz**

Baacke greift auf **Noam Chomsky** und **Jürgen Habermas** zurück. Jeder Mensch hat demnach eine grundlegende Fähigkeit zur Kommunikation (*Kompetenz*). Diese ist aber nicht gleichzusetzen mit dem, was jemand tatsächlich tut (*Performanz*):

> „Die bei jedem vorhandene Kompetenz muss zur Performanz gefördert werden“ (Meister & Burgfeld-Meise 2022, S. 881, mit Bezug auf Baacke 1996, S. 115–117).

Daraus folgt ein **pädagogischer Auftrag**: Medienkompetenz entwickelt sich nicht von selbst. Wer ökonomisch, sozial oder kulturell benachteiligt ist (Bourdieu), hat es schwerer, diese Fähigkeiten zu entwickeln (ebd.). Genau hier setzt Soziale Arbeit an.

</section>

    {{3}}
<section>

**Zielorientierung**

Medienkompetenz gilt in der Medienpädagogik als Leitbegriff und „Zielorientierung“ (Baacke 1996, S. 96, zit. n. Hugger 2022, S. 67). Das Modell beschreibt also, **wohin** pädagogisches Handeln führen soll – nicht, **wie** es konkret aussieht. Das „Wie“ entwickelst du in Abschnitt 7 selbst.

</section>

--{{1}}--
Baacke leitet Medienkompetenz aus der kommunikativen Kompetenz ab.

--{{2}}--
Kompetenz ist bei jedem Menschen angelegt, muss aber zur Performanz gefördert werden. Das ist der pädagogische Auftrag.


## Quiz: Herkunft des Begriffs

Aus welchem Begriff hat Baacke Medienkompetenz abgeleitet?

[( )] Informationstechnische Grundbildung
[(X)] Kommunikative Kompetenz
[( )] Computer Literacy
[( )] Digitale Souveränität
***
Baacke versteht Medienkompetenz als Ausdifferenzierung kommunikativer Kompetenz (Baacke 1973, 1996). Medien sind für ihn Mittel der Kommunikation und des Handelns, nicht in erster Linie Technik.
***

Was bedeutet die Unterscheidung von Kompetenz und Performanz für die Soziale Arbeit?

[( )] Medienkompetenz ist angeboren und muss nicht gefördert werden.
[( )] Nur Menschen mit hoher Bildung können Medienkompetenz entwickeln.
[(X)] Die Fähigkeit ist bei allen angelegt, ihre Entfaltung hängt aber von Förderung und Lebensbedingungen ab.
[( )] Performanz ist wichtiger als Kompetenz, deshalb zählt nur das Bedienen von Geräten.
***
Kompetenz ist bei jedem Menschen vorhanden, muss aber zur Performanz gefördert werden. Ob das gelingt, hängt von Lebensgeschichte, Motivation, Institutionen und sozialer Lage ab – ein klassisches Handlungsfeld der Sozialen Arbeit.
***

Vervollständige Baackes Definition: Medienkompetenz ist die Fähigkeit, in die Welt aktiv [[ (aneignender) | konsumierender | technischer ]] Weise auch alle Arten von Medien für das Kommunikations- und [[ (Handlungsrepertoire) | Freizeitverhalten | Wissensmanagement ]] von Menschen einzusetzen.


# 3 Die vier Dimensionen

Baacke (1996, S. 120) unterscheidet **vier Dimensionen** mit insgesamt **acht Unterdimensionen**, die „prinzipiell jeder Mensch entwickelt haben sollte“ (Hugger 2022, S. 68).

```ascii
                         +---------------------------+
                         |     MEDIENKOMPETENZ       |
                         |      (Baacke 1996)        |
                         +-------------+-------------+
                                       |
        +----------------+-------------+-------------+-------------------+
        |                |                           |                   |
+-------+------+ +-------+-------+         +---------+------+   +--------+-------+
| Medienkritik | |  Medienkunde  |         | Mediennutzung  |   | Mediengestaltung|
+--------------+ +---------------+         +----------------+   +----------------+
| analytisch   | | informativ    |         | rezeptiv-      |   | innovativ      |
| reflexiv     | | instrumentell-|         |   anwendend    |   | kreativ        |
| ethisch      | | qualifika-    |         | interaktiv-    |   |                |
|              | | torisch       |         |   anbietend    |   |                |
+--------------+ +---------------+         +----------------+   +----------------+

  Vermittlung (Kritik, Kunde)               Zielorientierung (Nutzung, Gestaltung)
```

Baacke (1997) ordnet Medienkritik und Medienkunde eher der **Vermittlung** zu, Mediennutzung und Mediengestaltung der **Zielorientierung** im Handeln der Menschen.

<div class="box warn">
<b>Häufiges Missverständnis:</b> "Medienethik" ist bei Baacke <i>keine</i> eigene fünfte Dimension. Die ethische Perspektive ist eine Unterdimension der <b>Medienkritik</b>.
</div>

Auf den folgenden Seiten lernst du jede Dimension einzeln kennen.


## Medienkritik

<div class="dim kritik">Medienkritik: analytisch – reflexiv – ethisch</div>

Medienkritik bedeutet nach Baacke (1996, S. 120; zit. n. Hugger 2022, S. 68) die Fähigkeit,

* **analytisch**: problematische gesellschaftliche Prozesse – etwa Medienkonzentration – „analytisch“ angemessen zu erfassen,
* **reflexiv**: dieses Wissen „reflexiv“ auf sich selbst und das eigene Handeln anzuwenden,
* **ethisch**: „analytisches Denken und reflexiven Rückbezug als sozial verantwortet“ abzustimmen und zu definieren.

**Medienkritik als Querschnittskompetenz:** Baacke betrachtet Medienkritik als eine „zu Medienkunde, Mediennutzung und Mediengestaltung quer liegende Kompetenz“ (Baacke 1997, S. 98–99, zit. n. Niesyto 2022, S. 125). Kritik soll also nicht isoliert geübt werden, sondern in jedem Umgang mit Medien mitlaufen.

**Beispiele aus der Sozialen Arbeit**

| Unterdimension | Beispiel |
| :------------- | :------- |
| analytisch     | Jugendliche untersuchen, warum ihnen eine Plattform bestimmte Videos vorschlägt und wer daran verdient. |
| reflexiv       | Eine Wohngruppe reflektiert die eigene Bildschirmzeit und wie sich Likes auf die Stimmung auswirken. |
| ethisch        | Eine Gruppe diskutiert, ob man ein peinliches Foto einer Mitschülerin weiterleiten darf. |

<div class="box ok">
<b>Merksatz:</b> Medienkritik fragt: Wie funktionieren Medien gesellschaftlich – was machen sie mit mir – und was ist verantwortliches Handeln?
</div>


## Medienkunde

<div class="dim kunde">Medienkunde: informativ – instrumentell-qualifikatorisch</div>

Medienkunde meint das **Wissen über das gegenwärtige Mediensystem** (Baacke 1996, S. 120; zit. n. Hugger 2022, S. 68–69). Sie hat zwei Seiten:

* **informativ**: klassische Wissensbestände, z. B. über Filmgenres, über die Funktionsweise von Suchmaschinen oder über den Unterschied zwischen öffentlich-rechtlichem und privatem Rundfunk,
* **instrumentell-qualifikatorisch**: die **Bedienungsfähigkeit**, also Geräte und Software handhaben können.

**Beispiele aus der Sozialen Arbeit**

| Unterdimension | Beispiel |
| :------------- | :------- |
| informativ     | Jugendliche wissen, was Influencer-Marketing ist und dass Werbung gekennzeichnet werden muss. |
| instrumentell-qualifikatorisch | Eine Seniorin lernt, im Messenger die Privatsphäre-Einstellungen zu ändern. |

<div class="box warn">
<b>Achtung, Verengung:</b> In der Praxis wird Medienkompetenz oft auf "Bedienkompetenz" reduziert. Genau davor warnt die Fachdiskussion – die instrumentell-qualifikatorische Unterdimension ist nur eine von acht.
</div>

<div class="box ok">
<b>Merksatz:</b> Medienkunde fragt: Was weiß ich über Medien – und wie bediene ich sie?
</div>


## Mediennutzung

<div class="dim nutzung">Mediennutzung: rezeptiv-anwendend – interaktiv-anbietend</div>

Mediennutzung ist nach Baacke (1996, S. 120; zit. n. Hugger 2022, S. 69) zweifach zu verstehen:

* **rezeptiv, anwendend**: Medienangebote wahrnehmen, auswählen und verarbeiten – z. B. eine Nachricht lesen und verstehen, einen Film anschauen (Baacke nennt das auch "Programm-Nutzungskompetenz"),
* **interaktiv, anbietend**: Medien aktiv und im Austausch nutzen – z. B. in Foren antworten, Online-Banking erledigen, sich an einer Online-Petition beteiligen, Inhalte teilen.

**Beispiele aus der Sozialen Arbeit**

| Unterdimension | Beispiel |
| :------------- | :------- |
| rezeptiv-anwendend | Ein Klient findet über eine Website die passende Beratungsstelle und versteht die Informationen. |
| interaktiv-anbietend | Jugendliche kommentieren in einem Stadtteil-Forum die Planung eines neuen Skateparks. |

<div class="box ok">
<b>Merksatz:</b> Mediennutzung fragt: Wie nehme ich Medien auf – und wie handle ich mit ihnen im Austausch mit anderen?
</div>


## Mediengestaltung

<div class="dim gestaltung">Mediengestaltung: innovativ – kreativ</div>

Mediengestaltung ist nach Baacke (1996, S. 120; zit. n. Hugger 2022, S. 69)

* **innovativ**: im Sinne von Veränderungen und Weiterentwicklungen des Mediensystems innerhalb seiner Logik,
* **kreativ**: in ästhetischer Weise über die „Grenzen der Kommunikationsroutine hinausgehen“ können.

Hier liegt der Kern der **handlungsorientierten Medienarbeit**: Menschen werden vom Konsumieren zum Produzieren gebracht. Medienprojekte wie Handyfilm, Fotoprojekt, Podcast oder Digital Storytelling werden dieser Dimension zugeordnet (vgl. Friedrichs-Liesenkötter & von Gross 2022).

**Beispiele aus der Sozialen Arbeit**

| Unterdimension | Beispiel |
| :------------- | :------- |
| innovativ | Eine Jugendgruppe entwickelt ein eigenes Instagram-Format, das Informationen der Jugendberatung jugendgerecht aufbereitet. |
| kreativ   | Geflüchtete Jugendliche erzählen ihre Geschichte als Fotostory oder Digital Story. |

<div class="box ok">
<b>Merksatz:</b> Mediengestaltung fragt: Wie bringe ich mich mit Medien selbst ein – und gehe dabei über das Gewohnte hinaus?
</div>


## Quiz: Dimensionen zuordnen

Ordne jede Aussage der passenden Dimension zu.

<!-- data-randomize -->
[[Medienkritik] [Medienkunde] [Mediennutzung] [Mediengestaltung]]
[      ( )            (X)            ( )              ( )        ] Ich weiß, wie man ein Video auf dem Smartphone schneidet.
[      (X)            ( )            ( )              ( )        ] Ich frage mich, welche Interessen hinter einer Nachrichtenseite stehen.
[      ( )            ( )            (X)            ( )        ] Ich beantrage meinen Personalausweis online.
[      ( )            ( )            ( )              (X)        ] Wir drehen einen eigenen Kurzfilm über unseren Stadtteil.
[      (X)            ( )            ( )              ( )        ] Ich überlege, ob ich ein Foto meiner Freundin ohne Erlaubnis posten darf.
[      ( )            (X)            ( )              ( )        ] Ich kenne den Unterschied zwischen einer Werbeanzeige und einem redaktionellen Beitrag.
[      ( )            ( )            (X)            ( )        ] Ich diskutiere in einem Forum über ein Computerspiel.
***
Bedienwissen und Wissen über Medien gehören zur Medienkunde. Hinterfragen und ethisches Abwägen gehören zur Medienkritik. Medien zur Erledigung von Aufgaben und im Austausch nutzen ist Mediennutzung. Selbst produzieren ist Mediengestaltung.
***

Zu welcher **Unterdimension** gehört: „Eine Jugendliche merkt, dass sie sich nach dem Scrollen durch Fitness-Accounts schlechter fühlt, und denkt darüber nach, warum.“

[( )] Medienkritik – analytisch
[(X)] Medienkritik – reflexiv
[( )] Medienkritik – ethisch
[( )] Mediennutzung – rezeptiv-anwendend
***
Hier wird das Wissen über Medienwirkungen auf sich selbst und das eigene Erleben bezogen – das ist die reflexive Unterdimension der Medienkritik.
***

Welche Dimension liegt nach Baacke „quer“ zu den anderen drei?

[[Medienkritik]]
[[?]] Sie sollte bei jedem Umgang mit Medien mitlaufen.
***
Medienkritik ist nach Baacke (1997, S. 98–99) eine zu Medienkunde, Mediennutzung und Mediengestaltung quer liegende Kompetenz.
***


# 4 Anwendung: Fälle aus der Praxis

Medienkompetenz zeigt sich in konkreten Situationen. Bearbeite die folgenden Fallvignetten. Überlege jeweils: **Welche Dimensionen sind betroffen – und welche müssten gefördert werden?**

<div class="box study">
Es gibt bei den Fällen meist mehrere sinnvolle Antworten. Die Auflösung zeigt eine Musterlösung – vergleiche sie mit deiner eigenen Begründung.
</div>


## Fall 1: Jugendtreff und Kurzvideos

Im Jugendtreff verbringen viele Besucher\*innen (13–16 Jahre) die meiste Zeit mit Kurzvideo-Apps. Ein Mitarbeiter bemerkt, dass einige Jugendliche Inhalte eines Influencers teilen, der Frauen abwertet und schnelles Geld durch fragwürdige Geschäftsmodelle verspricht. Die Jugendlichen finden ihn „einfach lustig“.

Welche Dimensionen sollten hier **vorrangig** gefördert werden?

[[X]] Medienkritik – analytisch (Geschäftsmodelle, Algorithmen, Reichweite verstehen)
[[X]] Medienkritik – ethisch (Abwertung anderer erkennen und bewerten)
[[ ]] Medienkunde – instrumentell-qualifikatorisch (App bedienen)
[[X]] Mediengestaltung – kreativ (eigene Gegen-Inhalte produzieren)
***
Die Jugendlichen können die App bereits bedienen – Bedienkompetenz ist nicht das Problem. Es fehlt an kritischer Einordnung: Wie verdient der Influencer Geld? Warum wird mir das angezeigt? Wen werten die Inhalte ab? Ein gestalterischer Zugang (z. B. eigene Videos, die das Format parodieren) kann Kritik erfahrbar machen, ohne zu moralisieren.
***


## Fall 2: Wohngruppe und Cybermobbing

In einer Wohngruppe der Jugendhilfe wird ein 14-jähriges Mädchen in einer Klassen-Chatgruppe beleidigt. Ein Foto von ihr wurde bearbeitet und verbreitet. Sie weiß nicht, wie sie reagieren soll, und will das Handy „am liebsten wegwerfen“.

Welche Dimensionen sind betroffen?

[[X]] Medienkunde – informativ (Rechte am eigenen Bild, Melde- und Hilfewege kennen)
[[X]] Medienkunde – instrumentell-qualifikatorisch (Screenshots sichern, Personen blockieren, melden)
[[X]] Medienkritik – ethisch (mit der Gruppe über Verantwortung und Mitläufer sprechen)
[[ ]] Mediengestaltung – innovativ
***
Kurzfristig braucht die Jugendliche Wissen und Handlungsfähigkeit (Medienkunde): Was ist erlaubt, wie sichere ich Beweise, wo bekomme ich Hilfe? Mittelfristig ist die ethische Dimension der Medienkritik für die ganze Gruppe zentral. Soziale Arbeit hat hier zudem einen Schutzauftrag – Medienkompetenzförderung ersetzt keine Intervention.
***


## Fall 3: Seniorentreff und Messenger

In einem Seniorentreff möchten mehrere Besucher\*innen (70–85 Jahre) mit ihren Enkeln per Messenger in Kontakt bleiben. Einige haben bereits Nachrichten mit Gewinnspielen und angeblichen Paketbenachrichtigungen erhalten und darauf geklickt.

Ordne die Lernbedarfe zu.

[[Medienkritik] [Medienkunde] [Mediennutzung]]
[      ( )           (X)           ( )      ] Wissen, wie man Fotos und Sprachnachrichten verschickt.
[      (X)           ( )           ( )      ] Betrugsnachrichten anhand typischer Merkmale erkennen und hinterfragen.
[      ( )           ( )           (X)      ] Regelmäßig in der Familiengruppe schreiben und Videoanrufe führen.
***
Die Bedienung gehört zur Medienkunde, das kritische Prüfen von Nachrichten zur Medienkritik (analytisch), der kommunikative Austausch mit der Familie zur Mediennutzung (interaktiv). Medienkompetenz ist eine Aufgabe lebenslangen Lernens – nicht nur ein Thema für Jugendliche.
***


## Fall 4: Desinformation

In einer Elterngruppe einer Familienberatungsstelle kursiert eine Sprachnachricht, nach der eine Impfung „heimlich Chips“ enthalte. Einige Eltern sind verunsichert, andere leiten die Nachricht weiter.

Beschreibe in eigenen Worten, wie ein Angebot **alle vier Dimensionen** ansprechen könnte (je ein Stichpunkt pro Dimension):

    [[___ ___ ___ ___ ___]]

Vergleiche anschließend mit dem Beispiel:

    {{1}}
<section>

| Dimension | Möglicher Ansatz |
| :-------- | :--------------- |
| Medienkritik | Wie entstehen Gerüchte? Wer profitiert davon? Warum leite ich so etwas weiter? Verantwortung beim Teilen. |
| Medienkunde | Faktencheck-Seiten kennen, Quellen prüfen (z. B. die Schritte zum Einschätzen einer Quelle von klicksafe), Rückwärts-Bildersuche bedienen. |
| Mediennutzung | Vertrauenswürdige Informationsquellen gezielt nutzen; im Gruppenchat sachlich reagieren. |
| Mediengestaltung | Gemeinsam eine eigene „Fake News“ erstellen, um die Mechanismen zu durchschauen; eine kurze Info-Sprachnachricht für den Elternchat produzieren. |

</section>


# 5 Kritik und Weiterentwicklungen

Baackes Modell ist bis heute Bezugspunkt, wurde aber vielfach diskutiert und weiterentwickelt. Die Positionen unterscheiden sich dabei „weniger in der grundsätzlichen Anerkennung, dass Medienkompetenz einen zentralen Zielwert der Medienpädagogik darstelle, sondern eher in der Art, wie ihre unterschiedlichen Teil-Dimensionen zu fassen sind“ (Hugger 2022, S. 69).

    {{1}}
<section>

**Zentrale Kritikpunkte**

* **Normative Unschärfe:** Das Modell sagt, *was* Menschen können sollten, aber kaum, *wie viel* und *woran* man das erkennt. Es muss präzisiert werden (z. B. Aufenanger, Schorb, Sutter, Tulodziecki; vgl. Hugger 2022).
* **Fehlende Altersdifferenzierung:** Theunert (1999) fordert, Medienkompetenz entwicklungsbezogen und altersspezifisch zu fassen – ein Kind braucht anderes als ein Erwachsener.
* **Verengung in der Praxis:** In bildungspolitischen Programmen wird Medienkompetenz oft auf Bedienkompetenz reduziert – entgegen Baackes Anspruch.
* **Soziale Ungleichheit:** Medienkompetenz ist sozial ungleich verteilt. Wer wenig ökonomisches, soziales und kulturelles Kapital hat (Bourdieu), hat schlechtere Startbedingungen (Meister & Burgfeld-Meise 2022).
* **Medienkritik unter neuen Bedingungen:** Datafizierung, Algorithmen, Künstliche Intelligenz und digitale Ungleichheit verlangen, Medienkritik neu zu konturieren. Niesyto (2020, S. 35) stellt fest, dass Medienkritik lange ein „Schattendasein“ geführt habe, und kritisiert bisherige Konzepte als oft „rationalitätslastig“ (S. 45).

</section>

    {{2}}
<section>

**Weiterentwicklungen und verwandte Modelle**

| Ansatz | Kernidee |
| :----- | :------- |
| Groeben (2002) | Sieben Dimensionen, u. a. „medienbezogene Genussfähigkeit“ und „Anschlusskommunikation“ |
| Dewe & Sander (1996) | Medienkompetenz als Sach-, Selbst- und Sozialkompetenz (Erwachsenenbildung) |
| Tulodziecki (1998; Tulodziecki et al. 2010) | „sachgerecht“, „selbstbestimmt“, „kreativ“ und „sozial verantwortlich“ handeln; fünf Aufgabenbereiche |
| Medienbildung (z. B. Tulodziecki 2015, Schorb 2009) | Medienbildung als Prozessbegriff, Medienkompetenz als Zielbeschreibung – „zwei Seiten derselben Medaille“ (Hugger 2007) |
| KMK (2016), DigComp (EU) | Bildungspolitische Kompetenzrahmen für die „digitale Welt“; Kritik: Gefahr hohler Labels |

</section>

    {{3}}
<section>

**Reflexionsfrage**

Welcher Kritikpunkt ist für dein Arbeitsfeld in der Sozialen Arbeit am wichtigsten – und warum?

    [[___ ___ ___]]

</section>


## Quiz: Kritik

Welche Aussagen geben Kritik bzw. Weiterentwicklungen des Baacke-Modells korrekt wieder?

[[X]] Theunert fordert eine altersdifferenzierte Konzeption von Medienkompetenz.
[[X]] Unter Bedingungen von Algorithmen und KI muss Medienkritik neu gefasst werden.
[[ ]] Baackes Modell wurde vollständig durch DigComp ersetzt und gilt als überholt.
[[X]] Medienkompetenz hängt auch von sozialer Lage und verfügbarem Kapital ab.
[[ ]] Kritiker*innen bemängeln, dass Baacke die Bedienkompetenz vergessen hat.
***
Baackes Modell ist weiterhin zentraler Bezugspunkt. Bedienkompetenz ist Teil der Medienkunde (instrumentell-qualifikatorisch) – kritisiert wird eher die Verengung auf diese Unterdimension in der Praxis.
***


# 6 Lernziele formulieren

Ein medienpädagogisches Angebot braucht klare Ziele. Das Baacke-Modell hilft, **welche** Kompetenz gefördert werden soll. Lernziele beschreiben, **woran** man sieht, dass es gelungen ist.

**Operationalisierte Lernziele** enthalten:

1. **Wer?** – die Zielgruppe („Die Teilnehmenden …“)
2. **Was?** – ein beobachtbares Verhalten (aktives Verb)
3. **Woran?** – der Inhalt bzw. Gegenstand
4. **Unter welchen Bedingungen?** – optional: Hilfsmittel, Rahmen, Umfang

> **Beispiel:** „Die Teilnehmenden (*wer*) unterscheiden (*was*) anhand von drei Prüffragen (*Bedingung*) zuverlässige von fragwürdigen Online-Informationen (*woran*).“

<div class="box warn">
<b>Vermeide Verben, die man nicht beobachten kann</b>, z. B. <i>verstehen, wissen, kennen, sich bewusst sein, stärken</i>. Sie eignen sich für übergeordnete Richtziele, aber nicht für überprüfbare Lernziele.
</div>


## Verben je Dimension

| Dimension | Passende Verben (Beispiele) |
| :-------- | :-------------------------- |
| Medienkritik – analytisch | analysieren, untersuchen, vergleichen, Interessen benennen, Merkmale identifizieren |
| Medienkritik – reflexiv | beschreiben (eigene Nutzung), begründen, Wirkungen an sich selbst darstellen |
| Medienkritik – ethisch | bewerten, abwägen, Regeln aushandeln, Position beziehen |
| Medienkunde – informativ | benennen, erklären, unterscheiden, zuordnen |
| Medienkunde – instrumentell-qualifikatorisch | einstellen, durchführen, sichern, bedienen, installieren |
| Mediennutzung – rezeptiv-anwendend | auswählen, recherchieren, Informationen entnehmen |
| Mediennutzung – interaktiv-anbietend | kommentieren, sich beteiligen, kommunizieren, teilen, veröffentlichen |
| Mediengestaltung – innovativ | ein Format entwickeln, umgestalten, weiterentwickeln |
| Mediengestaltung – kreativ | produzieren, gestalten, inszenieren, erzählen, drehen, aufnehmen |


## Gute und schlechte Lernziele

Welches Lernziel ist **operationalisiert**?

[( )] Die Jugendlichen werden für die Gefahren des Internets sensibilisiert.
[( )] Die Teilnehmenden verstehen, wie Algorithmen funktionieren.
[(X)] Die Teilnehmenden stellen in ihrem eigenen Messenger-Profil die Sichtbarkeit von Profilbild und Status auf "Meine Kontakte" ein.
[( )] Die Gruppe hat Spaß an Medien.
***
Nur das dritte Ziel benennt ein beobachtbares Verhalten (einstellen), einen Gegenstand (Sichtbarkeit von Profilbild und Status) und einen Rahmen (eigenes Profil). Es gehört zur Medienkunde (instrumentell-qualifikatorisch).
***

Ordne die Lernziele der Dimension zu, die sie **hauptsächlich** fördern.

<!-- data-randomize -->
[[Medienkritik] [Medienkunde] [Mediennutzung] [Mediengestaltung]]
[      (X)            ( )            ( )              ( )        ] Die Teilnehmenden vergleichen zwei Werbevideos und benennen die eingesetzten Überzeugungsstrategien.
[      ( )            ( )            ( )              (X)        ] Die Teilnehmenden produzieren in Kleingruppen einen zweiminütigen Podcast über ihren Lieblingsort im Stadtteil.
[      ( )            (X)            ( )              ( )        ] Die Teilnehmenden erklären mit eigenen Worten, was ein Cookie ist.
[      ( )            ( )            (X)            ( )        ] Die Teilnehmenden recherchieren mit einer Suchmaschine drei Beratungsangebote in ihrer Stadt.


## Übung: Eigene Lernziele

Wähle eine Zielgruppe aus deinem (künftigen) Arbeitsfeld und formuliere **zwei operationalisierte Lernziele**, die unterschiedliche Dimensionen fördern.

Meine Zielgruppe:

    [[___]]

Lernziel 1 (mit Angabe der Dimension und Unterdimension):

    [[___ ___]]

Lernziel 2 (mit Angabe der Dimension und Unterdimension):

    [[___ ___]]

**Selbstcheck** für deine Lernziele:

- [ ] Die Zielgruppe ist genannt.
- [ ] Das Verb beschreibt ein beobachtbares Verhalten.
- [ ] Der Inhalt bzw. Gegenstand ist konkret.
- [ ] Die Zuordnung zur Baacke-Dimension ist begründbar.
- [ ] Das Ziel ist im Rahmen des Angebots erreichbar.


# 7 Eigenes Angebot entwickeln

Jetzt verbindest du alles: Du skizzierst ein **medienpädagogisches Angebot** für eine Zielgruppe der Sozialen Arbeit. Die Struktur orientiert sich an der Vorlage für medienpädagogische Angebote aus dem Seminar.

1. Thema (Sachanalyse, Bezug zur Medienkompetenz, Ziele)
2. Zielgruppe (Beschreibung, Rahmenbedingungen, Relevanz der Ziele)
3. Ablauf
4. Materialbedarf
5. Umgang mit Schwierigkeiten
6. Evaluation
7. Quellen

Auf der nächsten Seite findest du einen Ideenpool mit Methoden, danach ein Kurzbeispiel und anschließend deine Arbeitsfelder.


## Ideenpool: Methoden

| Methode | Einsatzfeld | Ziele | Vorrangig geförderte Dimension(en) |
| :------ | :---------- | :---- | :--------------------------------- |
| Handyfilm / Kurzfilm | Jugendarbeit, Wohngruppen, Arbeit mit Geflüchteten | Ausdruck, Partizipation, Teamarbeit | Mediengestaltung, Medienkunde |
| Fotoprojekt / Foto-Erkundung | alle Felder | Selbstwirksamkeit, Perspektivwechsel, Stadtteilarbeit | Mediengestaltung, Medienkritik (reflexiv) |
| Podcast / Audio | Jugendarbeit, Hochschule, Reha | Stimme geben, Reflexion, Öffentlichkeit herstellen | Mediengestaltung, Mediennutzung (anbietend) |
| Social-Media-Analyse | Suchtarbeit, Beratung, Jugendarbeit | kritische Medienreflexion, Algorithmuskritik | Medienkritik (analytisch, reflexiv) |
| Digital Storytelling | Migration, Inklusion, Jugendhilfe | Biografie, Identität, Sprache | Mediengestaltung (kreativ), Medienkritik (reflexiv) |
| Erklärvideos | Beratungsstellen, Arbeit mit Geflüchteten | Sprachförderung, Wissenstransfer | Mediengestaltung, Medienkunde |
| Comics / visuelle Medien | Kinder, Menschen mit Lernschwierigkeiten | niedrigschwelliger Ausdruck | Mediengestaltung (kreativ) |
| Games / digitale Streetwork | Jugendarbeit, Streetwork | Beziehungsaufbau, Lebensweltorientierung | Mediennutzung, Medienkritik |
| Fake-News-Werkstatt | Jugendarbeit, Elternarbeit | Desinformation durchschauen | Medienkritik, Medienkunde, Mediengestaltung |
| Smartphone-Sprechstunde | Seniorenarbeit, Quartiersarbeit | digitale Teilhabe | Medienkunde (instrumentell), Mediennutzung |

<div class="box study">
<b>Tipp:</b> Ein gutes Angebot fördert nicht "alles", sondern setzt einen klaren Schwerpunkt auf eine oder zwei Dimensionen. Denke an die Medienkritik als Querschnittskompetenz: Auch ein Filmprojekt sollte eine Reflexionsphase enthalten.
</div>


## Kurzbeispiel: „Sicher, fair und selbstbestimmt online“

| Baustein | Inhalt |
| :------- | :----- |
| **Zielgruppe** | Jugendliche von 14–18 Jahren (Jugendhaus, Schulsozialarbeit), 10–18 Teilnehmende, 90–120 Min. |
| **Bezug zu Baacke** | Medienkritik: Inhalte, Quellen und Plattformlogiken hinterfragen. Medienkunde: Rechte, Privatsphäre-Einstellungen und Meldewege kennen. Mediennutzung: Plattformen zielgerichtet und verantwortungsvoll nutzen. Mediengestaltung: eigene Positionen in konstruktiven Formaten ausdrücken. |
| **Lernziele (Auswahl)** | Die Teilnehmenden unterscheiden zuverlässige von fragwürdigen Online-Informationen. Die Gruppe entwickelt gemeinsame Regeln für respektvolle digitale Kommunikation. |
| **Ablauf** | Einstieg (15') Blitzlicht „Was nervt euch online am meisten?“ – Input (20') Cybermobbing, Desinformation, Datenschutz – Fallarbeit (25') – Praxiswerkstatt (25') „Notfallkarten“ – Transfer (15') drei Gruppenregeln |
| **Material** | Moderationskarten, Beamer, Arbeitsblätter mit Fallvignetten, Handout mit Beratungsstellen |
| **Schwierigkeiten** | Betroffene in der Gruppe: Fälle anonymisieren, Rückzugsmöglichkeit, Ansprechperson für Einzelgespräche |
| **Evaluation** | Kurzabfrage am Ende, Notfallkarten als Ergebnis, Nachfrage nach zwei Wochen |

Ergänzend kann der sozialpädagogische Dreiklang aus **Prävention, Partizipation und Schutzauftrag** einbezogen werden.


## Arbeitsblatt: Mein Angebot

Fülle die Felder aus. Stichpunkte genügen. **Denke daran, die Ergebnisse zu kopieren.**

**1 Thema und Titel des Angebots**

    [[___ ___]]

**2 Zielgruppe** (Alter, Einrichtung, Lebenslage, Medienerfahrung)

    [[___ ___ ___]]

**3 Rahmenbedingungen** (Gruppengröße, Zeit, Raum, Technik, Team, freiwillig oder verpflichtend)

    [[___ ___ ___]]

**4 Bezug zu Baacke**: Welche Dimension(en) und Unterdimension(en) stehen im Mittelpunkt – und warum gerade diese für diese Zielgruppe?

    [[___ ___ ___ ___]]

**5 Lernziele** (2–4 operationalisierte Ziele, jeweils mit Dimension)

    [[___ ___ ___ ___]]

**6 Ablauf** (Phasen mit Zeitangaben: Einstieg – Erarbeitung – Produktion/Übung – Reflexion – Abschluss)

    [[___ ___ ___ ___ ___ ___]]

**7 Material**

    [[___ ___]]

**8 Umgang mit Schwierigkeiten** (z. B. unterschiedliche Vorkenntnisse, Technik fällt aus, persönliche Betroffenheit, Datenschutz und Bildrechte)

    [[___ ___ ___]]

**9 Evaluation**: Woran erkennst du, dass deine Lernziele erreicht wurden?

    [[___ ___ ___]]


## Selbstcheck: Mein Angebot

Prüfe deine Skizze kritisch:

- [ ] Die Zielgruppe und ihre Lebenswelt sind konkret beschrieben.
- [ ] Ich habe einen klaren Schwerpunkt auf eine oder zwei Dimensionen gelegt.
- [ ] Jedes Lernziel ist operationalisiert und einer Dimension zugeordnet.
- [ ] Die Methoden im Ablauf passen zu den Lernzielen – sie fördern die genannten Dimensionen wirklich.
- [ ] Es gibt eine Reflexionsphase (Medienkritik als Querschnittskompetenz).
- [ ] Das Angebot reduziert Medienkompetenz nicht auf Bedienkompetenz.
- [ ] Ich habe Zugangshürden bedacht (Ausstattung, Sprache, Vorwissen, soziale Lage).
- [ ] Datenschutz, Bildrechte und Schutzauftrag sind berücksichtigt.
- [ ] Die Evaluation prüft die Lernziele und nicht nur die Zufriedenheit.

Welcher Punkt fiel dir am schwersten?

    [[___ ___]]


# 8 Abschluss

## Abschlussquiz

Wie viele Dimensionen und Unterdimensionen umfasst Baackes Modell?

[( )] 3 Dimensionen, 6 Unterdimensionen
[(X)] 4 Dimensionen, 8 Unterdimensionen
[( )] 5 Dimensionen, 10 Unterdimensionen
[( )] 4 Dimensionen, 12 Unterdimensionen

Die Bedienungsfähigkeit von Geräten gehört zur Dimension [[ Medienkritik | (Medienkunde) | Mediennutzung | Mediengestaltung ]], und zwar zur [[ informativen | (instrumentell-qualifikatorischen) | rezeptiven ]] Unterdimension.

Welche Aussagen treffen zu?

[[X]] Medienkritik umfasst bei Baacke eine analytische, reflexive und ethische Unterdimension.
[[ ]] Medienethik ist bei Baacke eine eigenständige fünfte Dimension.
[[X]] Handlungsorientierte Medienprojekte fördern vor allem die Mediengestaltung.
[[X]] Mediennutzung umfasst rezeptiv-anwendende und interaktiv-anbietende Nutzung.

Ein Angebot, in dem Seniorinnen lernen, Betrugs-SMS an typischen Merkmalen zu erkennen, fördert vor allem …

[( )] Mediengestaltung – kreativ
[(X)] Medienkritik – analytisch
[( )] Mediennutzung – interaktiv-anbietend
[( )] Medienkunde – instrumentell-qualifikatorisch

Warum ist Medienkompetenzförderung ein Thema der Sozialen Arbeit?

[[X]] Weil Medienkompetenz sozial ungleich verteilt ist und gefördert werden muss.
[[X]] Weil gesellschaftliche Teilhabe zunehmend über Medien stattfindet.
[[ ]] Weil Medienkompetenz angeboren ist und sich von selbst entwickelt.
[[X]] Weil Adressat*innen in ihrer Lebenswelt mit Medienrisiken und -chancen konfrontiert sind.


## Reflexion

Erinnere dich an deine Selbsteinschätzung am Anfang. Was meinst du jetzt, wenn du „Medienkompetenz“ sagst? Welche Dimension möchtest du bei dir selbst weiterentwickeln?

    [[___ ___ ___]]

Wie hilfreich war diese Selbstlerneinheit für dich?

- [(1)] sehr hilfreich
- [(2)] hilfreich
- [(3)] teils, teils
- [(4)] wenig hilfreich


## Literatur

Baacke, D. (1973). *Kommunikation und Kompetenz. Grundlegung einer Didaktik der Kommunikation und ihrer Medien*. München: Juventa.

Baacke, D. (1996). Medienkompetenz – Begrifflichkeit und sozialer Wandel. In A. von Rein (Hrsg.), *Medienkompetenz als Schlüsselbegriff* (S. 112–124). Bad Heilbrunn: Klinkhardt.

Baacke, D. (1997). *Medienpädagogik*. Tübingen: Niemeyer.

Baacke, D. (1999). Projekte als Formen der Medienarbeit. In D. Baacke, S. Kornblum, J. Lauffer, L. Mikos & G. A. Thiele (Hrsg.), *Handbuch Medien: Medienkompetenz* (S. 31–35). Bonn: Bundeszentrale für politische Bildung.

Dewe, B., & Sander, U. (1996). Medienkompetenz und Erwachsenenbildung. In A. von Rein (Hrsg.), *Medienkompetenz als Schlüsselbegriff*. Bad Heilbrunn: Klinkhardt.

Friedrichs-Liesenkötter, H., & von Gross, F. (2022). Erzieherischer Kinder- und Jugendmedienschutz. In U. Sander, F. von Gross & K.-U. Hugger (Hrsg.), *Handbuch Medienpädagogik* (2. Aufl.). Wiesbaden: Springer VS. https://doi.org/10.1007/978-3-658-23578-9_105

Groeben, N. (2002). Dimensionen der Medienkompetenz: Deskriptive und normative Aspekte. In N. Groeben & B. Hurrelmann (Hrsg.), *Medienkompetenz. Voraussetzungen, Dimensionen, Funktionen* (S. 160–197). Weinheim/München: Juventa.

Hugger, K.-U. (2022). Medienkompetenz. In U. Sander, F. von Gross & K.-U. Hugger (Hrsg.), *Handbuch Medienpädagogik* (2. Aufl., S. 67–80). Wiesbaden: Springer VS. https://doi.org/10.1007/978-3-658-23578-9_9

Hugger, K.-U. (2007). Medienkompetenz. In U. Sander, F. von Gross & K.-U. Hugger (Hrsg.), *Handbuch Medienpädagogik* (1. Aufl., S. 93–99). Wiesbaden: VS.

Kultusministerkonferenz (2016). *Bildung in der digitalen Welt. Strategie der Kultusministerkonferenz*. Berlin: KMK.

Meister, D. M., & Burgfeld-Meise, B. (2022). Medienkompetenzförderung. In U. Sander, F. von Gross & K.-U. Hugger (Hrsg.), *Handbuch Medienpädagogik* (2. Aufl.). Wiesbaden: Springer VS. https://doi.org/10.1007/978-3-658-23578-9_99

Niesyto, H. (2020). Medienkritik und Medienpädagogik. *MedienPädagogik, 37*, 23–50. https://doi.org/10.21240/mpaed/37/2020.07.02.X

Niesyto, H. (2022). Medienkritik. In U. Sander, F. von Gross & K.-U. Hugger (Hrsg.), *Handbuch Medienpädagogik* (2. Aufl., S. 125 ff.). Wiesbaden: Springer VS. https://doi.org/10.1007/978-3-658-23578-9_14

Sander, U., von Gross, F., & Hugger, K.-U. (Hrsg.) (2022). *Handbuch Medienpädagogik* (2. Aufl.). Wiesbaden: Springer VS.

Theunert, H. (1999). Medienkompetenz: Eine pädagogische und altersspezifisch zu fassende Handlungsdimension. In F. Schell, E. Stolzenburg & H. Theunert (Hrsg.), *Medienkompetenz. Grundlagen und pädagogisches Handeln* (S. 50–59). München: kopaed.

Tulodziecki, G. (2015). Medienkompetenz. In F. von Gross, D. M. Meister & U. Sander (Hrsg.), *Medienpädagogik – ein Überblick* (S. 194–228). Weinheim/Basel: Beltz Juventa.

Tulodziecki, G., Herzig, B., & Grafe, S. (2010). *Medienbildung in Schule und Unterricht. Grundlagen und Beispiele*. Bad Heilbrunn: Klinkhardt.

**Weiterführend (online):** [klicksafe – Informationen und Materialien zu Medienkompetenz](https://www.klicksafe.de)
