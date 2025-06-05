---
layout: default
title: Puzzle 8 – Rekursive Funktionen (Fibonacci) [2D]
description: >-
  Implementiere die Fibonacci-Funktion rekursiv. Achte auf die
  korrekte Einrückung der Funktionsdefinition und Rückgabewerte.
---

<div id="p8-trash" class="sortable-code"></div>
<div id="p8-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p8-feedback" value="Get Feedback"  type="button" />
  <input id="p8-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "def fibonacci(n):\n" +
    "    if n <= 1:\n" +
    "        return n\n" +
    "    else:\n" +
    "        return fibonacci(n-1) + fibonacci(n-2)\n" +
    "print(fibonacci(6))\n" +
    "print(\"Fibonacci berechnet\")\n" +
    "return n + 1  #distractor\n" +
    "if n <= 0:  #distractor\n" +
    "fibonacci(n+1)  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p8-work",
    trashId:    "p8-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p8-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p8-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg7.html) | [Next](./aufg9.html)
