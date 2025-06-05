---
layout: default
title: Puzzle 5 – Lineare Algorithmen (Einfache Berechnung)
description: >-
  Ordne die Codezeilen so, dass das Programm zwei Zahlen einliest,
  sie addiert und das Ergebnis ausgibt.
---

<div id="p5-trash" class="sortable-code"></div>
<div id="p5-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p5-feedback" value="Get Feedback"  type="button" />
  <input id="p5-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "a = int(input(\"Erste Zahl: \"))\n" +
    "b = int(input(\"Zweite Zahl: \"))\n" +
    "summe = a + b\n" +
    "print(\"Die Summe ist:\", summe)\n" +
    "print(\"Fertig!\")\n" +
    "summe = a * b  #distractor\n" +
    "print(\"Fehler!\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p5-work",
    trashId:    "p5-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p5-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p5-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg4.html) | [Next](./aufg6.html)
