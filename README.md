<!--
author:   Jan Vanvinkenroye
email:    jan.vanvinkenroye@tik.uni-stuttgart.de
version:  1.3.0
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
/* EH-Logo statt LiaScript-Logo in der Kopfleiste (als Data-URI, weil
   relative Pfade in @style gegen liascript.github.io aufgeloest werden) */
.lia_header__logo {
  content: url("data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJFYmVuZV8xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB4PSIwcHgiIHk9IjBweCIgd2lkdGg9IjMwMnB4IiBoZWlnaHQ9IjE1M3B4IiB2aWV3Qm94PSIwIDAgMzAyIDE1MyIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgMzAyIDE1MyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+IDxwYXRoIGZpbGw9IiNFNzMzMzEiIGQ9Ik00NS40NzEsMTE0LjkwNWgtMC4wNThjMC4wNTQsMC4wMTgsMC4xMDQsMC4wNDMsMC4xNTMsMC4wN0w0NS40NzEsMTE0LjkwNXoiLz4gPGc+IDxwb2x5Z29uIGZpbGw9IiM1NzU3NTYiIHBvaW50cz0iMTU3LjkxNCw1Ni41NTUgMTQ5Ljc2OCw1Ni41NTUgMTQ5Ljc2OCw0OS45MTggMTU3LjIyLDQ5LjkxOCAxNTcuMjIsNDcuMTI0IDE0OS43NjgsNDcuMTI0IDE0OS43NjgsNDEuMzU5IDE1Ny42ODQsNDEuMzU5IDE1Ny42ODQsMzguNTY2IDE0Ni40NDUsMzguNTY2IDE0Ni40NDUsNTkuMzUgMTU3LjkxNCw1OS4zNSAiLz4gPHBvbHlnb24gZmlsbD0iIzU3NTc1NiIgcG9pbnRzPSIxNjYuNzk1LDU5LjM1IDE3MC45MjcsNDMuNjg4IDE2Ny41NzgsNDMuNjg4IDE2NS4xMDUsNTYuMDMyIDE2NS4wNDksNTYuMDMyIDE2Mi4zMTEsNDMuNjg4IDE1OC45MzYsNDMuNjg4IDE2My4xMjUsNTkuMzUgIi8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0xNzguMTE4LDQ5Ljc3M2wtMi4wMDksMC41NTNjLTIuNTAzLDAuNjk4LTQuMDc3LDEuNTQyLTQuMDc3LDUuMDM2YzAsMy4wMjgsMS41NDQsNC4zOTYsNC4wNzcsNC4zOTYgYzEuODYzLDAsMy4wNTctMC43NTcsMy45MDEtMi4zaDAuMDU4YzAuMDg0LDEuNTE0LDEuMjUyLDIuMDY3LDIuNjQ5LDIuMDY3YzAuNjEsMCwxLjE2My0wLjE3NSwxLjU0NC0wLjM3OVY1Ny4xMSBjLTAuMTE5LDAuMDU4LTAuMjkzLDAuMDg2LTAuNTI2LDAuMDg2Yy0wLjQ2NSwwLTAuODE0LTAuNTIyLTAuODE0LTEuMTA3di04Ljk2NmMwLTIuNzY2LTIuMjE2LTMuODQzLTQuOTc5LTMuODQzIGMtNC4xMzEsMC01LjUwMiwxLjgwNS01LjUwMiw1LjE1NGgyLjk3MmMwLTEuNTE0LDAuMjg4LTMsMi4zODgtM2MxLjY1OSwwLDIuMTUsMC45MDIsMi4xNSwyLjMzIEMxNzkuOTQ5LDQ5LjEzMiwxNzkuMjUsNDkuNDUzLDE3OC4xMTgsNDkuNzczeiBNMTc5Ljk0OSw1My43MDNjMCwyLjMzLTAuOTMsMy43MjYtMi44MjIsMy43MjZjLTEuMzA5LDAtMS45NS0xLjA0NS0xLjk1LTIuMzU2IGMwLTEuMzk5LDAuNDk1LTIuMzAxLDEuNzQ3LTIuNzM3bDEuMDE4LTAuMzVjMS4wMjEtMC4zNSwxLjQ4Ni0wLjU1MiwyLjAwOC0wLjkwMlY1My43MDN6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0xODkuMjY0LDQ4Ljg0MmMwLTIuMDk3LDEuMjI1LTMuMDU4LDIuNTA0LTMuMDU4YzEuNjMxLDAsMi4xODUsMC43MjksMi4xODUsMi44MjRWNTkuMzVoMy4xNDVWNDcuNTMxIGMwLTMuMTcyLTEuNTEzLTQuMjUtMy45MDEtNC4yNWMtMS43NDYsMC0zLjIzMiwwLjg0NC00LjAxNiwyLjI0MmgtMC4wODh2LTEuODM0aC0yLjk2OVY1OS4zNWgzLjE0MVY0OC44NDJ6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0yMTEuMzMsNTguNTkyVjQzLjY4N2gtMi45Njl2MS45MjNoLTAuMDU3Yy0wLjI5My0xLjEzNi0xLjU3NC0yLjMyOC0zLjQzOC0yLjMyOCBjLTQuNDUzLDAtNC45NzksNC42MjgtNC45NzksOC4wNjRjMCw0LjMwOCwxLjA0OCw3Ljg4OSw0LjY4OCw3Ljg4OWMxLjUxNywwLDIuOTY4LTAuNzg2LDMuNTUxLTIuMTU1aDAuMDU5djIuNTMyIGMwLDEuODM0LTEuMDE4LDIuOTQxLTIuNjUsMi45NDFjLTEuMzk2LDAtMi4yNjktMC45MDItMi4yNjktMS44NjRoLTIuOTY4YzAsMS4yODIsMC41MjEsNC4wMTcsNS4xOCw0LjAxNyBDMjA5LjcwMSw2NC43MDcsMjExLjMzLDYyLjQwNiwyMTEuMzMsNTguNTkyeiBNMjA1LjQ3OSw1Ni43MzFjLTIuMzI3LDAtMi40NDYtMy4wMjgtMi40NDYtNS43MDhjMC0yLjkxMiwwLjM4LTUuMjM4LDIuNjQ5LTUuMjM4IGMyLjE4NSwwLDIuNTA0LDIuODIyLDIuNTA0LDUuMzg2QzIwOC4xODYsNTMuNjQ2LDIwNy45MjQsNTYuNzMxLDIwNS40NzksNTYuNzMxeiIvPiA8cGF0aCBmaWxsPSIjNTc1NzU2IiBkPSJNMjE5LjQyLDU5Ljc1OWMzLjQwOSwwLDUuNTAyLTIuMTI1LDUuNTAyLTUuNjQ4aC0yLjk2OWMwLDAuOTYxLTAuMjYxLDMuNDkzLTIuNTAzLDMuNDkzIGMtMi4zNTcsMC0yLjYyMi0yLjY3OS0yLjYyMi00Ljc3NXYtMC45MDJoOC4xODJ2LTEuNjU5YzAtNC4zMzctMS4xNjQtNi45ODctNS41MjktNi45ODdjLTQuODkxLDAtNS43OTMsNC4zNjctNS43OTMsOC40NzEgQzIxMy42ODgsNTkuMDAyLDIxNi44NTgsNTkuNzU5LDIxOS40Miw1OS43NTl6IE0yMTYuODI4LDQ5LjQ1MmMwLTIuMDM3LDAuNjQxLTQuMDE2LDIuNjIyLTQuMDE2YzEuNzc0LDAsMi40MTUsMS41MTQsMi40MTUsMy40OTMgdjAuODQ0aC01LjAzN1Y0OS40NTJ6Ii8+IDxyZWN0IHg9IjIyNy43NDgiIHk9IjM4LjU2NSIgZmlsbD0iIzU3NTc1NiIgd2lkdGg9IjMuMTQxIiBoZWlnaHQ9IjIwLjc4NCIvPiA8cmVjdCB4PSIyMzQuMjA1IiB5PSI0My42ODgiIGZpbGw9IiM1NzU3NTYiIHdpZHRoPSIzLjE0NSIgaGVpZ2h0PSIxNS42NjEiLz4gPHJlY3QgeD0iMjM0LjIwNSIgeT0iMzguMzMzIiBmaWxsPSIjNTc1NzU2IiB3aWR0aD0iMy4xNDUiIGhlaWdodD0iMy4xNDYiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTI0NC45NzUsNTkuNzU5YzMuMTQ1LDAsNS42MjEtMS40MjYsNS42MjEtNC43NzRjMC0yLjQ3Ni0xLjA3OC0zLjcyOC0zLjQwNS00LjUxNGwtMi4wMDgtMC42OTggYy0xLjY2My0wLjU4My0yLjIxNi0xLjA0OC0yLjIxNi0yLjMwMWMwLTEuNDg0LDAuOTktMi4wMzgsMi4yNDItMi4wMzhjMS42MzMsMCwyLjA2NiwxLjE2NSwyLjA2NiwyLjQxNnYwLjQwOWgyLjk2OHYtMC42OTggYzAtMS45NTItMC44OTgtNC4yOC00Ljg4OC00LjI4Yy0zLjI2LDAtNS4zNTYsMS4zNjgtNS4zNTYsNC4zMDdjMCwyLjUwNCwxLjAxOCwzLjY5NywzLjE3MSw0LjQ1NWwyLjczOCwwLjk1OSBjMS4xMzcsMC40MDksMS43MjEsMS4xNjcsMS43MjEsMi4zMDFjMCwxLjQyNy0wLjgxOCwyLjMtMi41NjUsMi4zYy0xLjgzMSwwLTIuNDQ2LTAuOTYtMi40NDYtMi43OTR2LTAuNDk1aC0yLjc5NXYwLjU4MyBDMjM5LjgyMiw1Ny45MjYsMjQxLjAxNyw1OS43NTksMjQ0Ljk3NSw1OS43NTl6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0yNjMuNDg5LDUzLjY0NmgtMi45NjhjMCwyLjMzLTAuNjExLDMuNzg0LTIuMzU3LDMuNzg0Yy0yLjI0MiwwLTIuNzA3LTIuMzU2LTIuNzA3LTUuOTA5IGMwLTMuNjk3LDAuNDk1LTUuOTA5LDIuNzM0LTUuOTA5YzEuODA0LDAsMi4xODQsMS43NzUsMi4xODQsMy4yODloMy4xNDVjMC0yLjQ3NS0xLjA0OC01LjYxOC01LjMyOC01LjYxOCBjLTQuNjI3LDAtNS44ODMsMy4zNDctNS44ODMsOC4yMzljMCw0Ljg5MSwxLjI4Miw4LjIzOSw1LjgyNCw4LjIzOUMyNjIuMDM0LDU5Ljc1OSwyNjMuMjU5LDU3LjQsMjYzLjQ4OSw1My42NDZ6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0yNzIuOTIzLDQzLjI4MmMtMS42MzIsMC0yLjk0LDAuNzg2LTMuODQzLDIuMTU0bC0wLjA4OS0wLjA1OXYtNi44MTJoLTMuMTQ1VjU5LjM1aDMuMTQ1VjQ4Ljg0MyBjMC0yLjA2OCwxLjIyMi0zLjA1OSwyLjUwMy0zLjA1OWMxLjYwMiwwLDIuMTg2LDAuNzU4LDIuMTg2LDIuODI1VjU5LjM1aDMuMTQxVjQ3LjUzMiBDMjc2LjgyLDQ0LjM1OSwyNzUuMzA3LDQzLjI4MiwyNzIuOTIzLDQzLjI4MnoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTI5MC43MzQsNTEuOTI3di0xLjY1OWMwLTQuMzM3LTEuMTY0LTYuOTg3LTUuNTI5LTYuOTg3Yy00Ljg5MSwwLTUuNzkzLDQuMzY3LTUuNzkzLDguNDcxIGMwLDcuMjUsMy4xNzEsOC4wMDcsNS43MzIsOC4wMDdjMy40MDksMCw1LjUwMi0yLjEyNSw1LjUwMi01LjY0OGgtMi45NjljMCwwLjk2MS0wLjI2MSwzLjQ5My0yLjUwMywzLjQ5MyBjLTIuMzU3LDAtMi42MTgtMi42NzktMi42MTgtNC43NzV2LTAuOTAySDI5MC43MzR6IE0yODIuNTU3LDQ5LjQ1MmMwLTIuMDM3LDAuNjM3LTQuMDE2LDIuNjE4LTQuMDE2IGMxLjc3NCwwLDIuNDE1LDEuNTE0LDIuNDE1LDMuNDkzdjAuODQ0aC01LjAzM1Y0OS40NTJ6Ii8+IDxwb2x5Z29uIGZpbGw9IiM1NzU3NTYiIHBvaW50cz0iMTQ5Ljc2OCw4MC44OTYgMTU1Ljg3OSw4MC44OTYgMTU1Ljg3OSw5MC41NiAxNTkuMTk3LDkwLjU2IDE1OS4xOTcsNjkuNzc0IDE1NS44NzksNjkuNzc0IDE1NS44NzksNzguMSAxNDkuNzY4LDc4LjEgMTQ5Ljc2OCw2OS43NzQgMTQ2LjQ0NSw2OS43NzQgMTQ2LjQ0NSw5MC41NiAxNDkuNzY4LDkwLjU2ICIvPiA8cGF0aCBmaWxsPSIjNTc1NzU2IiBkPSJNMTYxLjgxNSw4Mi43MjljMCw0Ljg5MSwxLjUxMyw4LjIzOSw1LjgyNSw4LjIzOWM0LjMzNCwwLDUuODUxLTMuMzQ4LDUuODUxLTguMjM5IHMtMS4zMTMtOC4yMzktNS44NTEtOC4yMzlDMTYzLjA5OCw3NC40OSwxNjEuODE1LDc3LjgzOCwxNjEuODE1LDgyLjcyOXogTTE3MC4zNDcsODIuNzI5YzAsMy45ODgtMC40MDcsNS45MDktMi43MDYsNS45MDkgYy0yLjI0MywwLTIuNjgxLTEuOTIxLTIuNjgxLTUuOTA5YzAtMy40NjQsMC40MzgtNS45MDksMi42ODEtNS45MDlDMTY5LjkzOSw3Ni44MiwxNzAuMzQ3LDc5LjI2NSwxNzAuMzQ3LDgyLjcyOXoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTE3NS4yOTIsODIuNzI5YzAsNC44OTIsMS4yODIsOC4yMzksNS44MjUsOC4yMzljMy45LDAsNS4xMjEtMi4zNTgsNS4zNTUtNi4xMTRoLTIuOTcyIGMwLDIuMzI4LTAuNjA2LDMuNzg1LTIuMzU3LDMuNzg1Yy0yLjIzOSwwLTIuNzA3LTIuMzU4LTIuNzA3LTUuOTFjMC0zLjY5NywwLjQ5NS01LjkxMSwyLjczNy01LjkxMSBjMS44MDUsMCwyLjE4NiwxLjc3NywyLjE4NiwzLjI5MWgzLjE0NWMwLTIuNDc1LTEuMDQ5LTUuNjE4LTUuMzMtNS42MThDMTc2LjU0Nyw3NC40OSwxNzUuMjkyLDc3LjgzOCwxNzUuMjkyLDgyLjcyOXoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTE5Mi4wNTksNzYuNjQ2bC0wLjA4OC0wLjA2di02LjgxMmgtMy4xNDVWOTAuNTZoMy4xNDVWODAuMDUyYzAtMi4wNjcsMS4yMjUtMy4wNTksMi41MDQtMy4wNTkgYzEuNjA0LDAsMi4xODQsMC43NTksMi4xODQsMi44MjVWOTAuNTZoMy4xNDVWNzguNzQxYzAtMy4xNzItMS41MTItNC4yNS0zLjktNC4yNUMxOTQuMjcxLDc0LjQ5LDE5Mi45NjEsNzUuMjc2LDE5Mi4wNTksNzYuNjQ2eiIgLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTIxMi41NTEsNzkuNDY4di0wLjdjMC0xLjk1MS0wLjg5OC00LjI3OC00Ljg4OC00LjI3OGMtMy4yNjQsMC01LjM1NiwxLjM2OS01LjM1Niw0LjMwOCBjMCwyLjUwNCwxLjAxOCwzLjY5NywzLjE3Miw0LjQ1NGwyLjczNywwLjk2YzEuMTM2LDAuNDA5LDEuNzE2LDEuMTY2LDEuNzE2LDIuM2MwLDEuNDI3LTAuODEzLDIuMy0yLjU2MSwyLjMgYy0xLjgzNiwwLTIuNDQ1LTAuOTU4LTIuNDQ1LTIuNzkzdi0wLjQ5NmgtMi43OTV2MC41ODJjMCwzLjAyNywxLjE5Myw0Ljg2NCw1LjE1Miw0Ljg2NGMzLjE0NSwwLDUuNjE3LTEuNDI4LDUuNjE3LTQuNzc1IGMwLTIuNDc1LTEuMDc2LTMuNzI4LTMuNDA2LTQuNTE0bC0yLjAwOC0wLjY5OGMtMS42NTgtMC41ODMtMi4yMTEtMS4wNDgtMi4yMTEtMi4zYzAtMS40ODQsMC45OS0yLjAzOSwyLjI0Mi0yLjAzOSBjMS42MjcsMCwyLjA2NCwxLjE2NSwyLjA2NCwyLjQxNnYwLjQwOUgyMTIuNTUxeiIvPiA8cGF0aCBmaWxsPSIjNTc1NzU2IiBkPSJNMjIwLjQ5OCw3Ni44MThjMS44MDUsMCwyLjE4NiwxLjc3NywyLjE4NiwzLjI5MWgzLjE0NWMwLTIuNDc1LTEuMDQ5LTUuNjE4LTUuMzMtNS42MTggYy00LjYyNywwLTUuODgyLDMuMzQ4LTUuODgyLDguMjM5YzAsNC44OTIsMS4yODIsOC4yMzksNS44MjUsOC4yMzljMy45LDAsNS4xMjEtMi4zNTgsNS4zNTUtNi4xMTRoLTIuOTY4IGMwLDIuMzI4LTAuNjEsMy43ODUtMi4zNjEsMy43ODVjLTIuMjM5LDAtMi43MDctMi4zNTgtMi43MDctNS45MUMyMTcuNzYxLDc5LjAzMiwyMTguMjU2LDc2LjgxOCwyMjAuNDk4LDc2LjgxOHoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTIzMy44MDMsNzYuOTkzYzEuNTk3LDAsMi4xOCwwLjc1OSwyLjE4LDIuODI1VjkwLjU2aDMuMTQ1Vjc4Ljc0MWMwLTMuMTcyLTEuNTEyLTQuMjUtMy45LTQuMjUgYy0xLjYzMiwwLTIuOTQxLDAuNzg2LTMuODQ0LDIuMTU1bC0wLjA4OC0wLjA2di02LjgxMmgtMy4xNDFWOTAuNTZoMy4xNDFWODAuMDUyQzIzMS4yOTUsNzcuOTg0LDIzMi41Miw3Ni45OTMsMjMzLjgwMyw3Ni45OTN6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0yNTAuMDc0LDg4LjcyNWgwLjA4NHYxLjgzNGgyLjk2OVY3NC44OTdoLTMuMTQxdjEwLjk0NWMwLDEuNzQ4LTEuMTk1LDIuNjIxLTIuNTY1LDIuNjIxIGMtMS4zNjYsMC0yLjEyMy0wLjU4Mi0yLjEyMy0yLjMyOVY3NC44OTdoLTMuMTQ1djEwLjk0NWMwLDQuMDQ2LDEuNTcsNS4xMjYsMy45MDEsNS4xMjYgQzI0Ny44MDEsOTAuOTY5LDI0OS4yODcsOTAuMTIzLDI1MC4wNzQsODguNzI1eiIvPiA8cmVjdCB4PSIyNTYuMjk4IiB5PSI2OS43NzQiIGZpbGw9IiM1NzU3NTYiIHdpZHRoPSIzLjE0NSIgaGVpZ2h0PSIyMC43ODQiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTI3My40MTQsODUuMzJoLTIuOTY4YzAsMC45NjEtMC4yNjEsMy40OTQtMi41MDMsMy40OTRjLTIuMzU3LDAtMi42MTktMi42OC0yLjYxOS00Ljc3M3YtMC45MDRoOC4xNzggdi0xLjY1OWMwLTQuMzM2LTEuMTYyLTYuOTg2LTUuNTI4LTYuOTg2Yy00Ljg5MiwwLTUuNzk0LDQuMzY2LTUuNzk0LDguNDcxYzAsNy4yNSwzLjE3Miw4LjAwNiw1LjczMiw4LjAwNiBDMjcxLjMyMiw5MC45NjgsMjczLjQxNCw4OC44NDIsMjczLjQxNCw4NS4zMnogTTI2NS4zMjQsODAuNjYyYzAtMi4wMzcsMC42MzgtNC4wMTcsMi42MTktNC4wMTdjMS43NzMsMCwyLjQxNCwxLjUxNCwyLjQxNCwzLjQ5NCB2MC44NDNoLTUuMDMzVjgwLjY2MnoiLz4gPHBvbHlnb24gZmlsbD0iIzU3NTc1NiIgcG9pbnRzPSIxNDguMjI0LDk5LjQzMiAxNDYuMzYxLDk5LjQzMiAxNDYuMzYxLDEyMC4yMTcgMTU2Ljg0LDEyMC4yMTcgMTU2Ljg0LDExOC42NDQgMTQ4LjIyNCwxMTguNjQ0ICIvPiA8cGF0aCBmaWxsPSIjNTc1NzU2IiBkPSJNMTY2LjYxOSwxMTUuMTUzYzAsMi4zODYtMS4zOTgsMy45NTktMy4zNzUsMy45NTljLTEuODM2LDAtMi42OC0wLjk2Mi0yLjY4LTMuNDY2di0xMC44ODdoLTEuNzQ4djExLjY3MyBjMCwyLjkxMSwxLjYwMiw0LjEzNCwzLjk1OSw0LjEzNGMxLjU3NCwwLDMuMDg3LTAuNzg2LDMuOTYzLTIuNTAyaDAuMDU3djIuMTUzaDEuNTd2LTE1LjQ1OGgtMS43NDZWMTE1LjE1M3oiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTE3OS43MTksMTA3LjA4OWgtMC4wNTdjLTAuMzgxLTEuNjMtMS42ODktMi42NzktMy42MTMtMi42NzljLTMuNDA2LDAtNC45NDUsMi43MzYtNC45NDUsOC4wNjMgYzAsNS4zNTcsMS41MzksOC4wOTQsNC45NDUsOC4wOTRjMS44MzUsMCwzLjMxNi0xLjEzNywzLjc4NS0yLjkxMmgwLjA1OHYyLjU2MmgxLjU3Vjk5LjQzMmgtMS43NDNWMTA3LjA4OXogTTE3Ni4zNCwxMTkuMTEyIGMtMS43NDYsMC0zLjM3NS0wLjkwNS0zLjM3NS02LjY0YzAtNS43MDcsMS42MjktNi42MDksMy4zNzUtNi42MDljMS43NzgsMCwzLjM3OSwwLjkwMiwzLjM3OSw2LjYwOSBDMTc5LjcxOSwxMTguMjA3LDE3OC4xMTgsMTE5LjExMiwxNzYuMzQsMTE5LjExMnoiLz4gPHBvbHlnb24gZmlsbD0iIzU3NTc1NiIgcG9pbnRzPSIxOTUuNDM4LDExOC40NzEgMTk1LjM3NywxMTguNDcxIDE5Mi43NTgsMTA0Ljc1OSAxOTAuNjA0LDEwNC43NTkgMTg3LjgwOSwxMTguNDcxIDE4Ny43NTIsMTE4LjQ3MSAxODUuMTMzLDEwNC43NTkgMTgzLjI2NywxMDQuNzU5IDE4Ni43MDMsMTIwLjIxNyAxODguNzY5LDEyMC4yMTcgMTkxLjU2NCwxMDYuNTA1IDE5MS42MjEsMTA2LjUwNSAxOTQuNDE2LDEyMC4yMTcgMTk2LjQ4NiwxMjAuMjE3IDE5OS45MTgsMTA0Ljc1OSAxOTguMDU3LDEwNC43NTkgIi8+IDxyZWN0IHg9IjIwMi4wMTIiIHk9Ijk5LjQzMyIgZmlsbD0iIzU3NTc1NiIgd2lkdGg9IjEuNzQ2IiBoZWlnaHQ9IjIuOTY4Ii8+IDxyZWN0IHg9IjIwMi4wMTIiIHk9IjEwNC43NiIgZmlsbD0iIzU3NTc1NiIgd2lkdGg9IjEuNzQ2IiBoZWlnaHQ9IjE1LjQ1NyIvPiA8cGF0aCBmaWxsPSIjNTc1NzU2IiBkPSJNMjE1LjIzLDEwNy4xNDZoLTAuMDYyYy0wLjU1My0xLjc0NS0xLjkxOS0yLjczNi0zLjYwOC0yLjczNmMtMy40MDYsMC00Ljk0NSwyLjczNi00Ljk0NSw4LjA2MyBjMCw2LjE3MSwyLjM4NCw3Ljc0NCw0Ljc3MSw3Ljc0NGMxLjYwMiwwLDMuMDU3LTAuODc0LDMuNjA5LTIuNzY0aDAuMDU4djIuNDQ0YzAsMi43MzYtMS4xMzYsNC4yMjItMy4yNiw0LjIyMiBjLTEuNTQ0LDAtMi45MS0wLjg3NS0yLjkxLTIuMzNoLTEuNzQ3YzAuMDI3LDIuMjEzLDEuNjAyLDMuNzg0LDQuNiwzLjc4NGMzLjQ5NCwwLDUuMDY0LTIuMTgyLDUuMDY0LTYuNDYxdi0xNC4zNTNoLTEuNTdWMTA3LjE0NnogTTIxMS43NjgsMTE4Ljc2MmMtMi4wNywwLTMuMjk1LTEuNTE0LTMuMjk1LTYuNDY0YzAtNC45MiwxLjIyNS02LjQzNCwzLjI5NS02LjQzNGMyLjA2NSwwLDMuMjg2LDEuNTE0LDMuMjg2LDYuNDM0IEMyMTUuMDU0LDExNy4yNDgsMjEzLjgzMywxMTguNzYyLDIxMS43NjgsMTE4Ljc2MnoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTIyNi4wMjcsMTEyLjAzOGwtMi41MzQtMC45NjFjLTEuNzQzLTAuNjctMi4wOTctMS41MTQtMi4wOTctMi41OTFjMC0xLjU0MywwLjc4Ny0yLjYyMSwyLjgyNi0yLjYyMSBjMS42MDIsMCwyLjUzNCwwLjg0NiwyLjUzNCwyLjg1M3YwLjQzNmgxLjc0N3YtMC40MzZjMC0yLjgyMy0xLjM0LTQuMzA3LTQuMjU0LTQuMzA3Yy0yLjYxOSwwLTQuNTk2LDEuMjc5LTQuNTk2LDQuNDUyIGMwLDEuNTQ0LDAuNzgzLDIuODI1LDIuOTY3LDMuNjY5bDIuNDQ2LDAuOTYxYzEuNTQ0LDAuNjExLDIuMDk3LDEuNDg1LDIuMDk3LDIuODUzYzAsMS43MTgtMS4xOTQsMi43NjctMy4wNjEsMi43NjcgYy0xLjk3NywwLTIuOTY4LTEuMTY3LTIuOTY4LTMuNDM1di0wLjQwOWgtMS43NDd2MC40OTZjMCwzLjQ5MywxLjU3NCw0LjgwNCw0Ljc0Niw0LjgwNGMzLjI2NCwwLDQuNzc1LTEuOTUzLDQuNzc1LTQuNiBDMjI4LjkxLDExNC4yNzksMjI4LjEyMywxMTIuODI0LDIyNi4wMjcsMTEyLjAzOHoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTIzNi43MzksMTA0LjQxYy0xLjkyMywwLTMuMjMzLDEuMDQ3LTMuNjA4LDIuNjc5aC0wLjA1OXYtNy42NTdoLTEuNzV2MjAuNzg1aDEuNTc0di0yLjU2MmgwLjA1NyBjMC40NjUsMS43NzYsMS45NTEsMi45MTIsMy43ODYsMi45MTJjMy40MDUsMCw0Ljk0OS0yLjczNyw0Ljk0OS04LjA5M0MyNDEuNjg4LDEwNy4xNDYsMjQwLjE0NSwxMDQuNDEsMjM2LjczOSwxMDQuNDF6IE0yMzYuNDQ3LDExOS4xMTJjLTEuNzc3LDAtMy4zNzUtMC45MDQtMy4zNzUtNi42MzljMC01LjcwOCwxLjU5OC02LjYxLDMuMzc1LTYuNjFjMS43NDgsMCwzLjM3NSwwLjkwMiwzLjM3NSw2LjYxIEMyMzkuODIyLDExOC4yMDgsMjM4LjE5NSwxMTkuMTEyLDIzNi40NDcsMTE5LjExMnoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTI1Mi4yMjUsMTE1LjE1M2MwLDIuMzg2LTEuMzk4LDMuOTU5LTMuMzc1LDMuOTU5Yy0xLjgzNiwwLTIuNjgtMC45NjItMi42OC0zLjQ2NnYtMTAuODg3aC0xLjc0OHYxMS42NzMgYzAsMi45MTEsMS42MDIsNC4xMzQsMy45NTksNC4xMzRjMS41NzQsMCwzLjA4Ny0wLjc4NiwzLjk1OS0yLjUwMmgwLjA2MXYyLjE1M2gxLjU3di0xNS40NThoLTEuNzQ2VjExNS4xNTN6Ii8+IDxwYXRoIGZpbGw9IiM1NzU3NTYiIGQ9Ik0yNTkuMTUsMTA3LjE3NWgtMC4wNTh2LTIuNDE2aC0xLjc0N3YxNS40NThoMS43NDd2LTkuNjY0YzAtMywxLjgwNS00LjM5NiwzLjcyOS00LjM5NiBjMC4yNjEsMCwwLjU0OSwwLjAzLDAuODQxLDAuMDg2di0xLjc0NWMtMC4yMDMtMC4wNi0wLjQwNy0wLjA4OC0wLjYxLTAuMDg4QzI2MS4yNDcsMTA0LjQxLDI1OS44MjIsMTA1LjQ1OSwyNTkuMTUsMTA3LjE3NXoiLz4gPHBhdGggZmlsbD0iIzU3NTc1NiIgZD0iTTI3My40MTQsMTA3LjE0NmgtMC4wNTdjLTAuNTU0LTEuNzQ1LTEuOTItMi43MzYtMy42MDktMi43MzZjLTMuNDEsMC00Ljk0OSwyLjczNi00Ljk0OSw4LjA2MyBjMCw2LjE3MSwyLjM4OCw3Ljc0NCw0Ljc3MSw3Ljc0NGMxLjYwMiwwLDMuMDU3LTAuODc0LDMuNjEzLTIuNzY0aDAuMDU5djIuNDQ0YzAsMi43MzYtMS4xMzcsNC4yMjItMy4yNjQsNC4yMjIgYy0xLjU0LDAtMi45MS0wLjg3NS0yLjkxLTIuMzNoLTEuNzQ4YzAuMDMxLDIuMjEzLDEuNjA1LDMuNzg0LDQuNiwzLjc4NGMzLjQ5NCwwLDUuMDY0LTIuMTgyLDUuMDY0LTYuNDYxdi0xNC4zNTNoLTEuNTdWMTA3LjE0NnogTTI2OS45NTEsMTE4Ljc2MmMtMi4wNjksMC0zLjI5MS0xLjUxNC0zLjI5MS02LjQ2NGMwLTQuOTIsMS4yMjItNi40MzQsMy4yOTEtNi40MzRjMi4wNjUsMCwzLjI5MSwxLjUxNCwzLjI5MSw2LjQzNCBDMjczLjI0MiwxMTcuMjQ4LDI3Mi4wMTcsMTE4Ljc2MiwyNjkuOTUxLDExOC43NjJ6Ii8+IDwvZz4gPHBhdGggZmlsbD0iIzVDNUM1QiIgZD0iTTEyNC4xMTEsNjEuOTY4Yy0yLjYyNi0yLjQ1Ny02LjI0Ni0zLjY0My0xMC44NDYtMy41NjJjLTMuMDc2LDAuMDI0LTUuODY3LDAuNzUxLTguMzc1LDIuMTg4IGMtMi41MDcsMS40MzktNC42MDQsMy40NDQtNi4yOTMsNi4wMTZsLTAuMzMtMC4yMjNWMzguODk2SDg2LjI4OXY4MC43ODNoMTEuOTc5Vjc5LjZjMC4wOS0zLjg4NiwxLjA3MS02LjgwMSwyLjk0NS04Ljc0MiBjMS44NjktMS45NDYsNC4wNzQtMi45MTcsNi42MDctMi45MTdjMi45NzMtMC4wMzgsNS4xMSwwLjc4Niw2LjQyLDIuNDcxYzEuMzAxLDEuNjg0LDEuOTQ2LDQuNDQ5LDEuOTE2LDguMjk4djQwLjk2OWgxMS45NzlWNzQuNjAzIEMxMjguMDgyLDY4LjYzOCwxMjYuNzQyLDY0LjQyMywxMjQuMTExLDYxLjk2OCIvPiA8cGF0aCBmaWxsPSIjRTczMzMxIiBkPSJNNDguODA3LDEwOC43NzZsMC4wOTcsMC4wNzFjLTAuMDUyLTAuMDI2LTAuMS0wLjA1Mi0wLjE1My0wLjA3MUg0OC44MDd6IE00Ny44MDMsODEuOTQzIGMtMC4wNjMtNC4wNCwwLjY0Ni03LjU3MSwyLjEyNC0xMC41ODRjMS40NzktMy4wMTUsNC4xMDYtNC41OTgsNy44NzYtNC43NWMzLjM0OSwwLjA4MSw1LjczMiwxLjM2Miw3LjE1LDMuODMzIGMxLjQyMiwyLjQ3MywyLjExMSw1LjYzOCwyLjA3Miw5LjUwM3YzLjIxOUg0Ny44MDNWODEuOTQzeiBNNzkuMDAxLDkxLjM2OXYtNi4zMThjMC4xNjEtOC40MDMtMS4yNzEtMTQuOTIzLTQuMy0xOS41NyBjLTMuMDI5LTQuNjQ5LTguNjIzLTcuMDA2LTE2Ljc4Ny03LjA3NWMtNi4xODIsMC4xMDgtMTAuODY5LDEuNzQxLTE0LjA2Myw0Ljg5NmMtMy4xOTgsMy4xNTYtNS4zNTYsNy4xOC02LjQ2NiwxMi4wNzQgYy0wLjg5MSwzLjkwOS0xLjM4Myw3Ljk2LTEuNTEzLDEyLjE0NWMtMC4wMzQsMS4wNTQtMC4wNjIsMi4xMTEtMC4wNDQsMy4xODNjMCwwLjA4NiwwLjAwNCwwLjE2LDAuMDA0LDAuMjQ4IGMwLjEwNyw4Ljk1LDEuMjY5LDE1LjYwOCwzLjQ4OCwxOS45NTNjMi4yMyw0LjM2Nyw0Ljk5OCw3LjIwOCw4LjMwNSw4LjUzM2MwLjAxOCwwLjAwOCwwLjAzNCwwLjAyLDAuMDUsMC4wMjQgYzIuODM3LDEuMTIyLDUuNjg3LDEuNjg1LDguNTM5LDEuNzQ5YzAuNDkzLDAuMDE0LDAuOTg1LDAuMDQxLDEuNDc4LDAuMDIyYzYuNTU5LTAuMDY5LDExLjY4LTIuMDA3LDE1LjM2Mi01LjgwOSBzNS41NTItOS4wNDEsNS42MTctMTUuNzI1SDY3LjM1NWMwLjA0MywxLjI4Ni0wLjE1MSwyLjk2My0wLjU3Myw1LjAzNGMtMC40MjksMi4wNzctMS4zMjcsMy45NTQtMi42OTksNS42MzUgYy0xLjM3NCwxLjY3NS0zLjQ3LDIuNTY1LTYuMjgsMi42NjRjLTAuMzU0LTAuMDA4LTAuNjk4LTAuMDM0LTEuMDI4LTAuMDY3Yy0yLjQ0Ni0wLjI2MS00LjI5OC0xLjIxOS01LjU2Ny0yLjg3NSBjLTEuNDM0LTEuODkxLTIuMzczLTQuMjIzLTIuODExLTdjLTAuMTYxLTEuMDIyLTAuMjgtMi4wNDEtMC4zNzYtMy4wNTljLTAuMDA4LTAuMDc1LTAuMDE2LTAuMTUzLTAuMDIzLTAuMjI4IGMtMC4xLTEuMTMxLTAuMTQ5LTIuMjUxLTAuMTczLTMuMzc2Yy0wLjAxNC0wLjUzNy0wLjAyOS0xLjA3NS0wLjAyMS0xLjYxM3YtMy40NDRINzkuMDAxeiIvPiA8Zz4gPHBhdGggZmlsbD0iIzAwOEM0OCIgZD0iTTM3Ljc4NCwxMjAuMDU1Yy0wLjExMS0wLjE1OS0wLjIxNy0wLjM0MS0wLjMyNS0wLjUwNmMtMS41NDEtMS40NzgtMi45MjktMy4zOTMtNC4xNS01Ljc4MSBjLTEuMDgtMi4xMTgtMS45MDgtNC43OTMtMi40ODUtOC4wMDRDMTMuMjE1LDg5LjQyMyw2LjkxLDYzLjYwOSwxNy4wMzksNDEuMTEzYzEyLjc5Ny0yOC40Miw0Ni45NDUtNDAuNzUzLDc2LjI3MS0yNy41NDkgYzE2Ljg2Myw3LjU5NCwyOC40NDcsMjEuOTg0LDMyLjgyNCwzOC4yNDVjLTMuOTM5LTE4LjcyNi0xNi40NTItMzUuMzgxLTM1LjIzNi00My44MzlDNTkuNjU4LTYuMDk5LDIyLjkzLDcuODIzLDguODYxLDM5LjA2NCBDLTQuODczLDY5LjU2Niw4LjA4NCwxMDUuMjg5LDM3Ljc4NCwxMjAuMDU1eiIvPiA8cGF0aCBmaWxsPSIjMDA4QzQ4IiBkPSJNMTUzLjM2MSwxMzcuMTM3Yy0yNC43ODUsMC4yMjktNDkuNTcyLDAuNzk1LTc0LjM1MywxLjc4M2MtMjQuNzk2LDEuMDMzLTQ5LjUyMiwyLjMzNC03NC4zNDcsNC42NTggYy0wLjAyMSwwLTAuMDU1LDAuMDAzLTAuMDc0LDAuMDA3Yy0xLjgzMiwwLjIxMS0zLjE0NSwxLjg3LTIuOTMyLDMuNzAxYzAuMjEzLDEuODMyLDEuODcsMy4xNDUsMy43MDMsMi45M2wwLjA1OC0wLjAwOCBjMjQuNDQ2LTIuODQxLDQ5LjE3Ny00LjcwNyw3My44NDktNi4yODVjMjQuNjkyLTEuNTQzLDQ5LjQxOS0yLjY2NSw3NC4xNjQtMy40NTJjNDkuNDg4LTEuNTU5LDk5LjAzMy0xLjc4LDE0OC41NjMtMC44OTggQzI1Mi40OTIsMTM3LjU4LDIwMi45MzMsMTM2LjY4NiwxNTMuMzYxLDEzNy4xMzd6Ii8+IDwvZz4gPC9zdmc+");
  width: auto !important;
  height: 46px !important;
}
.lia-variant-dark .eh-svg-dunkel { fill: #BADFCC; }
.lia-variant-dark path.eh-svg-dunkel { fill: none; stroke: #BADFCC; }
/* Download-Button im Stil ehlb-button (dunkelgruen, weiss, Pfeil) */
.eh-download {
  background: var(--eh-dunkelgruen); color: white; border: 0;
  padding: 10px 16px; font: inherit; font-weight: 500; cursor: pointer;
}
.eh-download:hover, .eh-download:focus { background: var(--eh-gruen); }
.eh-download-status { margin-left: 0.8rem; font-size: 0.9em; }
@end

@onload
// Sammelt die Felder des Arbeitsblatts und bietet sie als Textdatei an.
// Gelesen wird direkt aus dem DOM, weil LiaScript Umfragewerte nicht
// ueber eine oeffentliche API herausgibt.
window.ehSkizzeDownload = function (button) {
  var labels = [
    "Name",
    "1 Thema und Titel des Angebots",
    "2 Zielgruppe",
    "3 Rahmenbedingungen",
    "4 Bezug zu Baacke",
    "5 Lernziele",
    "6 Ablauf",
    "7 Material",
    "8 Umgang mit Schwierigkeiten",
    "9 Evaluation"
  ];
  var root = button.closest("main") || document;
  var fields = root.querySelectorAll("textarea, input[type='text'], input:not([type])");
  var status = root.querySelector(".eh-download-status");
  var values = Array.prototype.map.call(fields, function (f) { return (f.value || "").trim(); });
  if (values.join("") === "") {
    if (status) status.textContent = "Die Felder sind noch leer.";
    return;
  }
  var datum = new Date().toLocaleDateString("de-DE");
  var text = "Angebotsskizze - Medienkompetenz nach Dieter Baacke\n"
    + "Selbstlerneinheit Medienpaedagogik, EH Ludwigsburg\n"
    + "Erstellt am " + datum + "\n\n";
  labels.forEach(function (label, i) {
    text += "== " + label + " ==\n" + (values[i] || "(leer)") + "\n\n";
  });
  var name = (values[0] || "").toLowerCase()
    .replace(/[äöüß]/g, function (c) { return {"ä":"ae","ö":"oe","ü":"ue","ß":"ss"}[c]; })
    .replace(/[^a-z0-9]+/g, "-").replace(/^-|-$/g, "");
  var blob = new Blob([text], { type: "text/plain;charset=utf-8" });
  var a = document.createElement("a");
  a.href = URL.createObjectURL(blob);
  a.download = "angebotsskizze" + (name ? "-" + name : "") + ".txt";
  document.body.appendChild(a);
  a.click();
  setTimeout(function () { URL.revokeObjectURL(a.href); a.remove(); }, 1000);
  if (status) status.textContent = "Datei wurde heruntergeladen.";
};
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
<b>Wichtig zum Speichern:</b> Deine Eingaben in Textfeldern werden nur lokal in deinem Browser gespeichert. Deine Angebotsskizze (Abschnitt 7) kannst du mit einem Button als Textdatei herunterladen und in Moodle abgeben. Deine Lernziele aus Abschnitt 6 kopierst du bei Bedarf selbst in ein eigenes Dokument.
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

<lia-keep>
<svg viewBox="0 0 1000 440" xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="dim-title dim-desc" style="width:100%;max-width:900px;height:auto;display:block;margin:1rem auto;font-family:'Barlow Semi Condensed',Barlow,Arial,sans-serif">
<title id="dim-title">Die vier Dimensionen von Medienkompetenz nach Baacke</title>
<desc id="dim-desc">Medienkompetenz gliedert sich in Medienkritik (analytisch, reflexiv, ethisch), Medienkunde (informativ, instrumentell-qualifikatorisch), Mediennutzung (rezeptiv-anwendend, interaktiv-anbietend) und Mediengestaltung (innovativ, kreativ). Medienkritik und Medienkunde gehoeren zur Vermittlung, Mediennutzung und Mediengestaltung zur Zielorientierung.</desc>
<rect x="370" y="15" width="260" height="76" fill="#054926"/>
<text x="500" y="50" text-anchor="middle" font-size="26" font-weight="500" fill="white">Medienkompetenz</text>
<text x="500" y="76" text-anchor="middle" font-size="17" font-weight="300" fill="white">nach Baacke (1996)</text>
<g stroke="#098C49" stroke-width="2.5" fill="none"><path d="M500 91 V122 M125 122 H875"/><path d="M125 122 V150"/><path d="M375 122 V150"/><path d="M625 122 V150"/><path d="M875 122 V150"/></g>
<rect x="20" y="150" width="210" height="52" fill="#098C49"/>
<text x="125" y="184" text-anchor="middle" font-size="22" font-weight="500" fill="white">Medienkritik</text>
<rect x="20" y="202" width="210" height="150" fill="#CEE8DB"/>
<rect x="38" y="227" width="7" height="7" fill="#098C49"/>
<text x="54" y="238" font-size="18" font-weight="400" fill="#212529">analytisch</text>
<rect x="38" y="259" width="7" height="7" fill="#098C49"/>
<text x="54" y="270" font-size="18" font-weight="400" fill="#212529">reflexiv</text>
<rect x="38" y="291" width="7" height="7" fill="#098C49"/>
<text x="54" y="302" font-size="18" font-weight="400" fill="#212529">ethisch</text>
<rect x="270" y="150" width="210" height="52" fill="#098C49"/>
<text x="375" y="184" text-anchor="middle" font-size="22" font-weight="500" fill="white">Medienkunde</text>
<rect x="270" y="202" width="210" height="150" fill="#CEE8DB"/>
<rect x="288" y="227" width="7" height="7" fill="#098C49"/>
<text x="304" y="238" font-size="18" font-weight="400" fill="#212529">informativ</text>
<rect x="288" y="259" width="7" height="7" fill="#098C49"/>
<text x="304" y="270" font-size="18" font-weight="400" fill="#212529">instrumentell-</text>
<text x="304" y="292" font-size="18" font-weight="400" fill="#212529">qualifikatorisch</text>
<rect x="520" y="150" width="210" height="52" fill="#098C49"/>
<text x="625" y="184" text-anchor="middle" font-size="22" font-weight="500" fill="white">Mediennutzung</text>
<rect x="520" y="202" width="210" height="150" fill="#CEE8DB"/>
<rect x="538" y="227" width="7" height="7" fill="#098C49"/>
<text x="554" y="238" font-size="18" font-weight="400" fill="#212529">rezeptiv-anwendend</text>
<rect x="538" y="259" width="7" height="7" fill="#098C49"/>
<text x="554" y="270" font-size="18" font-weight="400" fill="#212529">interaktiv-anbietend</text>
<rect x="770" y="150" width="210" height="52" fill="#098C49"/>
<text x="875" y="184" text-anchor="middle" font-size="22" font-weight="500" fill="white">Mediengestaltung</text>
<rect x="770" y="202" width="210" height="150" fill="#CEE8DB"/>
<rect x="788" y="227" width="7" height="7" fill="#098C49"/>
<text x="804" y="238" font-size="18" font-weight="400" fill="#212529">innovativ</text>
<rect x="788" y="259" width="7" height="7" fill="#098C49"/>
<text x="804" y="270" font-size="18" font-weight="400" fill="#212529">kreativ</text>
<path d="M20 368 V382 H480 V368" stroke="#054926" stroke-width="2" fill="none" class="eh-svg-dunkel"/>
<text x="250" y="414" text-anchor="middle" font-size="19" font-weight="500" fill="#054926" class="eh-svg-dunkel">Vermittlung</text>
<path d="M520 368 V382 H980 V368" stroke="#054926" stroke-width="2" fill="none" class="eh-svg-dunkel"/>
<text x="750" y="414" text-anchor="middle" font-size="19" font-weight="500" fill="#054926" class="eh-svg-dunkel">Zielorientierung</text>
</svg>
</lia-keep>

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

Fülle die Felder aus. Stichpunkte genügen. Am Ende lädst du deine Skizze als Textdatei herunter und gibst sie in der **Moodle-Aufgabe** ab.

**Dein Name**

    [[___]]

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

<div class="box">
<b>Abgeben:</b> Klicke auf den Button, um alle Felder dieser Seite als Textdatei zu speichern. Lade die Datei anschließend in der Moodle-Aufgabe zur Angebotsskizze hoch. Du musst die Felder dafür nicht einzeln abschicken.
</div>

<lia-keep>
<p><button class="eh-download" onclick="window.ehSkizzeDownload(this)">Meine Angebotsskizze herunterladen &rarr;</button><span class="eh-download-status" role="status"></span></p>
</lia-keep>


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
