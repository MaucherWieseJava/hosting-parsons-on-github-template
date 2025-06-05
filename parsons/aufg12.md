---
layout: default
title: Puzzle 12 – Rekursive Funktionen (Potenz-Berechnung)
description: >-
  Implementiere eine rekursive Funktion zur Berechnung von x^n
  (x hoch n) ohne die eingebaute pow()-Funktion zu verwenden.
---

<div id="p12-trash" class="sortable-code"></div>
<div id="p12-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p12-feedback" value="Get Feedback"  type="button" />
  <input id="p12-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "def potenz(x, n):\n" +
    "    if n == 0:\n" +
    "        return 1\n" +
    "    else:\n" +
    "        return x * potenz(x, n-1)\n" +
    "basis = 2\n" +
    "exponent = 4\n" +
    "ergebnis = potenz(basis, exponent)\n" +
    "print(f\"{basis}^{exponent} = {ergebnis}\")\n" +
    "return x + n  #distractor\n" +
    "if n == 1:  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p12-work",
    trashId:    "p12-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p12-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p12-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg11.html) | [Next](./aufg13.html)
