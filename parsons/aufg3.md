---
layout: default
title: Puzzle 3 – Schleife (Summe 1 … 10)
description: >-
  Setze die Codezeilen in die richtige Reihenfolge,
  um die Summe der Zahlen von 1 bis 10 auszugeben.
---

<div id="p3-trash" class="sortable-code"></div>
<div id="p3-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p3-feedback" value="Get Feedback"  type="button" />
  <input id="p3-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "total = 0\n" +
    "for i in range(1, 11):\n" +
    "    total += i\n" +
    "print(total)\n" +
    "i = 0  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p3-work",
    trashId:    "p3-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p3-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p3-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg2.html) | [Next](./aufg4.html)
