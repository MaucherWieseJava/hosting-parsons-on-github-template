---
layout: default
title: Puzzle 4 – Rekursion (Fakultät)
description: >-
  Bringe die Zeilen in die passende Reihenfolge,
  sodass die Funktion factorial(n) die Fakultät berechnet.
---

<div id="p4-trash" class="sortable-code"></div>
<div id="p4-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p4-feedback" value="Get Feedback"  type="button" />
  <input id="p4-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "def factorial(n):\\n" +
    "    if n == 0:\\n" +
    "        return 1\\n" +
    "    else:\\n" +
    "        return n * factorial(n - 1)\\n" +
    "return 0  #distractor\\n" +
    "print(factorial(5))\\n";

  var pp = new ParsonsWidget({
    sortableId: "p4-work",
    trashId:    "p4-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p4-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p4-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Next](./aufg5.html)
