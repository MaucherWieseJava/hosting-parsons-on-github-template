---
layout: default
title: Puzzle 13 – Lineare Algorithmen (Kreis-Berechnung)
description: >-
  Berechne Umfang und Fläche eines Kreises basierend auf dem
  eingegebenen Radius. Verwende die Konstante π (pi).
---

<div id="p13-trash" class="sortable-code"></div>
<div id="p13-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p13-feedback" value="Get Feedback"  type="button" />
  <input id="p13-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "import math\n" +
    "radius = float(input(\"Radius des Kreises: \"))\n" +
    "umfang = 2 * math.pi * radius\n" +
    "flaeche = math.pi * radius ** 2\n" +
    "print(f\"Umfang: {umfang:.2f}\")\n" +
    "print(f\"Fläche: {flaeche:.2f}\")\n" +
    "print(\"Berechnung abgeschlossen\")\n" +
    "umfang = math.pi * radius  #distractor\n" +
    "flaeche = 2 * radius  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p13-work",
    trashId:    "p13-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p13-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p13-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg12.html) | [Next](./aufg14.html)
