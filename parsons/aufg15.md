---
layout: default
title: Puzzle 15 – Schleifen (Primzahlen-Check) [2D]
description: >-
  Erstelle ein Programm, das prüft, ob eine Zahl eine Primzahl ist.
  Verwende eine for-Schleife mit korrekter Einrückung.
---

<div id="p15-trash" class="sortable-code"></div>
<div id="p15-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p15-feedback" value="Get Feedback"  type="button" />
  <input id="p15-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "zahl = int(input(\"Zahl eingeben: \"))\n" +
    "if zahl < 2:\n" +
    "    print(\"Keine Primzahl\")\n" +
    "else:\n" +
    "    ist_primzahl = True\n" +
    "    for i in range(2, int(zahl**0.5) + 1):\n" +
    "        if zahl % i == 0:\n" +
    "            ist_primzahl = False\n" +
    "            break\n" +
    "    if ist_primzahl:\n" +
    "        print(\"Ist eine Primzahl\")\n" +
    "    else:\n" +
    "        print(\"Keine Primzahl\")\n" +
    "for i in range(1, zahl):  #distractor\n" +
    "ist_primzahl = False  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p15-work",
    trashId:    "p15-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p15-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p15-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg14.html)
