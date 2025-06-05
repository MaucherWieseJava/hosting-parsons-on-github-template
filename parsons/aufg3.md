---
layout: default
title: Puzzle 3 – Schleifen (Summe 1 … 10)
---

Setze die Zeilen in die richtige Reihenfolge, um die Summe der Zahlen von 1 bis 10 zu berechnen.

<div id="loop-trash" class="sortable-code"></div>
<div id="loop-work"  class="sortable-code"></div>
<div style="clear: both;"></div>
<p>
    <input id="loop-feedback"  type="button" value="Feedback" />
    <input id="loop-reset"     type="button" value="Reset"    />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "total = 0\\n" +
    "for i in range(1, 11):\\n" +
    "    total += i\\n" +
    "print(total)\\n" +
    "i = 0  #distractor\\n";

  var pp = new ParsonsWidget({
    sortableId: "loop-work",
    trashId:    "loop-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#loop-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#loop-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Next](./aufg4.html)
