---
layout: default
title: Puzzle 11 – Schleifen (Multiplikationstabelle) [2D]
description: >-
  Erstelle eine Multiplikationstabelle für eine eingegebene Zahl
  mit verschachtelten Schleifen und korrekter Einrückung.
---

<div id="p11-trash" class="sortable-code"></div>
<div id="p11-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p11-feedback" value="Get Feedback"  type="button" />
  <input id="p11-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "zahl = int(input(\"Zahl für Multiplikationstabelle: \"))\n" +
    "print(f\"Multiplikationstabelle für {zahl}:\")\n" +
    "for i in range(1, 11):\n" +
    "    ergebnis = zahl * i\n" +
    "    print(f\"{zahl} x {i} = {ergebnis}\")\n" +
    "print(\"Tabelle vollständig\")\n" +
    "for i in range(1, 5):  #distractor\n" +
    "ergebnis = zahl + i  #distractor\n" +
    "print(\"Fehler!\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p11-work",
    trashId:    "p11-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p11-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p11-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg10.html) | [Next](./aufg12.html)
