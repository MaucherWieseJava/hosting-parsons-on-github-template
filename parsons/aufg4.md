---
layout: default
title: Puzzle 4 – Rekursion (Fakultät)
---

Bringe die Zeilen in die korrekte Reihenfolge, sodass die Funktion `factorial` die Fakultät einer Zahl berechnet.

<div id="fact-trash" class="sortable-code"></div>
<div id="fact-work"  class="sortable-code"></div>
<div style="clear: both;"></div>
<p>
    <input id="fact-feedback"  type="button" value="Feedback" />
    <input id="fact-reset"     type="button" value="Reset"    />
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
    sortableId: "fact-work",
    trashId:    "fact-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#fact-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#fact-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>
