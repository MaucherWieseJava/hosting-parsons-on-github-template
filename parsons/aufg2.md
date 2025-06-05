---
layout: default
title: Puzzle 2 – Verzweigung (if / else)
---

Ordne die Codezeilen so, dass das Programm entscheidet, ob eine Zahl gerade oder ungerade ist.

<div id="cond-trash" class="sortable-code"></div>
<div id="cond-work"  class="sortable-code"></div>
<div style="clear: both;"></div>
<p>
    <input id="cond-feedback"  type="button" value="Feedback" />
    <input id="cond-reset"     type="button" value="Reset"    />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "x = int(input(\"Gib eine Zahl ein:\"))\\n" +
    "if x % 2 == 0:\\n" +
    "    print(\"Gerade\")\\n" +
    "else:\\n" +
    "    print(\"Ungerade\")\\n" +
    "print(\"Zahl ist negativ\")  #distractor\\n";

  var pp = new ParsonsWidget({
    sortableId: "cond-work",
    trashId:    "cond-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#cond-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#cond-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>
