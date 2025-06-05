---
layout: default
title: Puzzle 6 – Verzweigungen (Temperatur-Check) [2D]
description: >-
  Erstelle ein Programm, das die Temperatur prüft und entsprechende
  Kleidungsempfehlungen gibt. Achte auf die richtige Einrückung!
---

<div id="p6-trash" class="sortable-code"></div>
<div id="p6-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p6-feedback" value="Get Feedback"  type="button" />
  <input id="p6-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "temp = int(input(\"Temperatur in Celsius: \"))\n" +
    "if temp < 0:\n" +
    "    print(\"Sehr kalt! Winterjacke anziehen.\")\n" +
    "elif temp < 15:\n" +
    "    print(\"Kühl. Jacke empfohlen.\")\n" +
    "elif temp < 25:\n" +
    "    print(\"Angenehm. Leichte Kleidung.\")\n" +
    "else:\n" +
    "    print(\"Warm! T-Shirt reicht.\")\n" +
    "print(\"Wetter-Check abgeschlossen.\")\n" +
    "if temp > 100:  #distractor\n" +
    "print(\"Fehlerhafte Eingabe\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p6-work",
    trashId:    "p6-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p6-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p6-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg5.html) | [Next](./aufg7.html)
