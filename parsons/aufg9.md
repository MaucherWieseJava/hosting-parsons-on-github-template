---
layout: default
title: Puzzle 9 – Lineare Algorithmen (Notendurchschnitt)
description: >-
  Berechne den Durchschnitt von drei Noten und gib eine
  entsprechende Bewertung aus.
---

<div id="p9-trash" class="sortable-code"></div>
<div id="p9-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p9-feedback" value="Get Feedback"  type="button" />
  <input id="p9-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "note1 = float(input(\"Erste Note: \"))\n" +
    "note2 = float(input(\"Zweite Note: \"))\n" +
    "note3 = float(input(\"Dritte Note: \"))\n" +
    "durchschnitt = (note1 + note2 + note3) / 3\n" +
    "print(\"Durchschnitt:\", round(durchschnitt, 2))\n" +
    "print(\"Berechnung abgeschlossen\")\n" +
    "durchschnitt = note1 + note2  #distractor\n" +
    "print(\"Fehler in Berechnung\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p9-work",
    trashId:    "p9-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p9-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p9-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg8.html) | [Next](./aufg10.html)
