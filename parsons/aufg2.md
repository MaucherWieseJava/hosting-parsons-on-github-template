---
layout: default
title: Puzzle 2 – Verzweigung (Gerade / Ungerade)
description: >-
  Ordne die Blöcke so, dass das Programm entscheidet,
  ob eine eingegebene Zahl gerade oder ungerade ist.
---

<div id="p2-trash" class="sortable-code"></div>
<div id="p2-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p2-feedback" value="Get Feedback"  type="button" />
  <input id="p2-reset"    value="Reset Problem" type="button" />
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
    sortableId: "p2-work",
    trashId:    "p2-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p2-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p2-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Next](./aufg3.html)
