---
layout: default
title: Puzzle 1 – Sequenzierung (Begrüßung)
---

Erstelle ein Programm, das den Namen einer Benutzerin abfragt und eine Begrüßung ausgibt.

<div id="greet-trash" class="sortable-code"></div>
<div id="greet-work"  class="sortable-code"></div>
<div style="clear: both;"></div>
<p>
    <input id="greet-feedback"  type="button" value="Feedback" />
    <input id="greet-reset"     type="button" value="Reset"    />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "name = input(\"Wie heißt du?\")\\n" +
    "print(\"Hallo, \" + name + \"!\")\\n" +
    "print(\"Auf Wiedersehen\")  #distractor\\n";

  var pp = new ParsonsWidget({
    sortableId: "greet-work",
    trashId:    "greet-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#greet-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#greet-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>
