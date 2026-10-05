# Ohmsches Gesetz — Simulations-Dashboard

Interaktive HTML-Simulation für den Unterricht (DE / FR / EN, hell / dunkel): ein **einfacher Gleichstromkreis** mit regelbarer Spannungsquelle U₀, Schalter S, Leitungen, Widerstand R, Amperemeter (Gesamtstrom) und Voltmeter (am Widerstand). Die Schülerinnen und Schüler sehen **Elektronenfluss und technische Stromrichtung** gleichzeitig, lesen U und I sofort ab oder nehmen eine **Messreihe** auf – mit Tabelle, Kennlinie I = f(U) und einer **schrittweisen Herleitung des Ohmschen Gesetzes** auf Knopfdruck.

🔗 **Live:** https://temmchen.github.io/ohm/

<img src="qr-code.png" alt="QR-Code zur Simulation" width="180">

`qr-code.png` / `qr-code.svg` = derselbe QR-Code wie in der Simulation (zum Ausdrucken oder für Folien).

## Was die Simulation zeigt

- **Schaltung** (links): Spannungsquelle U₀ (+ oben), Schalter S (anklickbar), Amperemeter A in Reihe, Widerstand R, Voltmeter V parallel zu R. Die Instrumente zeigen ihre Messwerte direkt im Schaltbild.
- **Elektronenfluss** (blaue Teilchen mit „−“) läuft **im Draht vom Minuspol zum Pluspol**, die **technische Stromrichtung** (orange Pfeile neben dem Draht) **vom Pluspol zum Minuspol**; beide Darstellungen sind einzeln zuschaltbar. Zwei Richtungsbögen in der Masche fassen das zusammen (I im Uhrzeigersinn, e⁻ dagegen). Bei offenem Schalter ruhen die Elektronen, in der Lücke gibt es keine. Das Tempo der Teilchen ist proportional zu I (Skala: volles Tempo bei U_max / R-Dekade, unter dem Schaltbild angegeben), damit „U verdoppeln → doppelt so schnell“ und „R verdoppeln → halb so schnell“ sichtbar wird.
- **Spannungsquelle – regelbar oder konstant** (Umschalter „Quelle“, Taste **K**):
  *regelbar* = Schieberegler von 0 bis zu einem frei wählbaren Maximum (1 … 1000 V), Schrittweite 0,1 … 10 V, Knöpfe − / + oder Pfeiltasten;
  *konstant* = feste Spannung als Zahl (Symbol ohne Verstellpfeil). Bei konstanter Quelle wird der **Widerstand** verändert: Die Messreihe
  trägt dann je R-Wert eine Zeile ein (R, I, R · I = U) und zeichnet die Kennlinie **I = f(R)** (Hyperbel: I umgekehrt proportional zu R);
  „Start“/„Schritt“ und die Herleitung gehören zum Experiment mit regelbarer Quelle und sind dort ausgeblendet. `?quelle=konstant` startet so.
- **Widerstand:** Zahlenwert plus Präfix **mΩ / Ω / kΩ / MΩ**.
- **Messung:** große Voltmeter-/Amperemeter-Anzeigen mit automatischem Präfix (µA … kA), darunter die Rechnung mit eingesetzten Zahlen, z. B. `I = U / R = 12 V / 4,7 kΩ = 12 V / 4 700 Ω = 0,00255 A = 2,55 mA`. Bei offenem Schalter: I = 0, Voltmeter am Widerstand 0 V – mit dem Hinweis, dass U₀ jetzt am offenen Schalter liegt.

### Modus „Sofort“ und Modus „Messreihe“

| | Verhalten |
|---|---|
| **Sofort** | Jede Änderung von U₀, R oder S wird unmittelbar in Schaltbild, Instrumenten und Rechnung angezeigt. |
| **Messreihe** | Jede Änderung von U₀ trägt automatisch einen Messwert (U, I, U/I) in die Tabelle ein. **Start** fährt U₀ selbsttätig von 0 bis zum Maximum (Tempo langsam / normal / schnell), **Schritt** geht einen Wert weiter. Rechts entsteht synchron die **Kennlinie I = f(U)**. Ein Klick auf eine Tabellenzeile oder einen Messpunkt stellt die Schaltung (Quelle, Instrumente, Teilchen) auf genau diesen Messwert. Wird R geändert, beginnt eine neue Reihe; bis zu drei Reihen bleiben im Diagramm (je flacher, desto größer R). **Kopieren** legt die Tabelle als Tab-getrennten Text in die Zwischenablage (Excel / Numbers). |

### Herleitung des Ohmschen Gesetzes (per Knopfdruck)

Sobald mindestens drei Messwerte vorliegen, wird der Knopf **„Herleitung des Ohmschen Gesetzes“** aktiv. Die Herleitung erscheint **nicht automatisch**, sondern Schritt für Schritt („Nächster Schritt“ / „Alle Schritte“) – immer mit den **Zahlen der aktuellen Messreihe**:

1. **Beobachtung** – U wird verdoppelt (Faktor k), I wächst um denselben Faktor.
2. **Quotient prüfen** – I / U ist in jeder Zeile gleich ⇒ I ~ U (Proportionalität).
3. **Kennlinie als Funktion** – Gerade ⇒ lineare Funktion I = m · U + b; wegen I(0) = 0 ist b = 0 ⇒ Ursprungsgerade I = m · U (proportionale Funktion; FR: fonction affine → fonction linéaire).
4. **Proportionalitätsfaktor = Steigung** – m = ΔI / ΔU am Steigungsdreieck (wird im Diagramm eingezeichnet), Einheit A/V = S (Leitwert G).
5. **Widerstand als Kehrwert** – R = 1 / m = ΔU / ΔI = U / I (die Tabellenspalte U / I).
6. **Ohmsches Gesetz** – I = U / R, U = R · I, R = U / I; ohmscher Widerstand = Ursprungsgerade als Kennlinie (G. S. Ohm, 1826).

Während der Herleitung zeigt das Diagramm nur die aktuelle Reihe, damit das Steigungsdreieck lesbar ist.

## Im Unterricht

- **Beamer:** Taste **F** = Vollbild, **S** = Schalter, **+ / −** (oder Pfeiltasten) = U₀ schrittweise, **Leertaste** = Messreihe starten/anhalten, **E** / **T** = Elektronen bzw. technische Stromrichtung ein/aus, **M** = Modus, **K** = Quelle regelbar/konstant, **Q** = QR-Code bildschirmfüllend, **H** = Tastaturhilfe. Passt auf 1024×768, 1280×800 und 1920×1080; auf dem Handy (375 px) einspaltig.
- **Sprache:** DE / FR / EN umschaltbar (wird gemerkt); `?lang=fr` bzw. `?lang=en` startet direkt in der Sprache. Zahlen erscheinen mit dem Dezimaltrennzeichen der Sprache (12,5 V bzw. 12.5 V).
- **Startwerte per Adresse:** `?umax=24&step=2&r=4700&u=6&zu=1&modus=reihe&quelle=konstant` (Maximum, Schrittweite, R in Ω, U₀, Schalter geschlossen, Modus Messreihe, konstante Quelle) – z. B. für einen vorbereiteten Link im Journal.
- Hell/Dunkel folgt dem System und ist umschaltbar (wird gemerkt).

## Didaktische Konventionen

- Ideale Instrumente (Amperemeter 0 Ω, Voltmeter ∞), ideale Quelle; R temperaturunabhängig – es geht um das Gesetz, nicht um Messfehler.
- Das Voltmeter liegt **am Widerstand**: bei offenem Schalter zeigt es 0 V (U₀ liegt am Schalter). Diese Falle ist bewusst Teil der Simulation.
- Technische Stromrichtung = Vereinbarung (+ → −), Elektronen bewegen sich tatsächlich − → +; beide werden nie vermischt dargestellt (Pfeile neben dem Draht, Teilchen im Draht).
- Taxonomie-/Kompetenzzuordnung erfolgt im zugehörigen Aufgabenblatt, nicht in der Simulation.

## Technik

Eine einzige Datei `index.html`, Vanilla JS + SVG, keine Abhängigkeiten, kein Build. Der QR-Code (Version 3, Fehlerkorrektur M, mit CoreImage gegengeprüft) ist als SVG-Pfad eingebettet. Tastaturbedienbar, `prefers-reduced-motion` wird respektiert (Teilchen ruhen, Werte bleiben), Tabelle als Text-Zwilling des Diagramms, Farbpalette für Farbfehlsichtigkeit geprüft (hell und dunkel).

```bash
open index.html
```

---

## Section française (résumé)

Simulation interactive de la **loi d'Ohm** : circuit simple avec source de tension réglable U₀, interrupteur S, résistance R, ampèremètre et voltmètre. Les élèves voient en même temps le **flux d'électrons** (du − vers le +, dans le fil) et le **sens conventionnel du courant** (du + vers le −, flèches le long du fil) ; la vitesse des particules est proportionnelle à I. La tension se règle de 0 à un maximum choisi, par pas réglables ; la résistance se saisit avec son préfixe (mΩ … MΩ). La source est **réglable** ou **constante** (à tension constante, on fait varier R : tableau R, I, R · I = U et caractéristique I = f(R)). Mode **Instantané** (affichage immédiat de U et I avec le calcul) ou mode **Série de mesures** : chaque valeur de U₀ ajoute une ligne au tableau (U, I, U/I) et un point à la **caractéristique I = f(U)** ; « Démarrer » parcourt automatiquement toute la plage. Un bouton **« Établir la loi d'Ohm »** déroule ensuite, étape par étape et avec les valeurs mesurées, la démarche : observation (U doublée ⇒ I doublée) → quotient I/U constant ⇒ proportionnalité → droite = fonction affine I = a·U + b avec b = 0 ⇒ fonction linéaire → coefficient de proportionnalité = pente ΔI/ΔU (conductance, siemens) → résistance R = 1/a = U/I → loi d'Ohm. Trois langues (FR / DE / EN), mode clair / sombre, code QR (touche Q) pour ouvrir la page sur le téléphone.

## English (summary)

Interactive **Ohm's law** simulation: simple DC circuit with adjustable or constant source U₀ (constant source: vary R, table and I = f(R) characteristic), switch, resistor (value + prefix mΩ … MΩ), ammeter and voltmeter. Electron flow and conventional current are shown side by side; particle speed is proportional to I. Instant readings with the worked calculation, or a measurement series with table, I = f(U) characteristic and a step-by-step, button-triggered derivation of Ohm's law (proportionality → straight line through the origin → slope = constant of proportionality → R = U/I). DE / FR / EN, light / dark, QR code (key Q).

## Lizenz

MIT — © 2026 Tom Bleyer
