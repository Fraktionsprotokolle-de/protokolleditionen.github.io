---
layout: post
title: 'Relaunch von fraktionsprotokolle.de'
categories: [Aktuelles]
---

**Relaunch von fraktionsprotokolle.de: Wechsel vom teiPublisher zu einem eignen Static Site Generator**

Die Kommission für [Geschichte des Parlamentarismus und der politischen Parteien (KGParl)](https://kgparl.de/) hat die digitale Edition »Fraktionen im Deutschen Bundestag. Sitzungsprotokolle 1949 bis 2005« unter [fraktionsprotokolle.de](https://fraktionsprotokolle.de) technisch und gestalterisch vollständig neu aufgestellt. Das bisherige System auf Basis des teiPublisher wurde durch einen eigenen Static Site Generator (SSG) abgelöst, dessen Quellcode unter einer MIT-Lizenz öffentlich zugänglich ist: [github.com/Fraktionsprotokolle-de/kgparl-protokolle-ssg](https://github.com/Fraktionsprotokolle-de/kgparl-protokolle-ssg).

<!--more-->

Der Build-Prozess transformiert [TEI-XML-Quellen aus dem öffentlichen Repositorium der Edition](https://github.com/Fraktionsprotokolle-de/fraktionsprotokolle_web) mittels XSLT in statische HTML-Seiten. Als Build-Framework kommt Apache Ant in Verbindung mit dem DSE-Static-Cookiecutter des ACDH-CH zum Einsatz. Die Volltextsuche wird über Typesense mit InstantSearch.js realisiert; das Frontend verwendet Tailwind v4. Indexierungsskripte sind in Python und Go implementiert; Build- und Deployment-Prozesse laufen über Shell-Skripte und ein Makefile, das Live- und Test-Umgebungen über eine zentrale `environments.json` steuert.

Die Einleitungstexte der einzelnen Fraktionseditionen sind nun integral in die Website eingebunden und vollständig durchsuchbar. Das Personenregister wurde überarbeitet und mit Daten aus dem Open-Data-Portal des Deutschen Bundestags angereichert. Neu eingeführt wurde ein Schlagwortregister, das die thematische Erschließung der Protokolle systematisch voranbringen soll; die Erschließung wächst kontinuierlich und wird schrittweise auf den gesamten Bestand ausgedehnt.
