---
layout: default
title: Puzzle 1 – Sequenzierung (Begrüßung)
description: >-
  Ziehe oder mische die Codeblöcke, um ein Programm zusammenzustellen,
  das den Namen einer Benutzerin abfragt und eine Begrüßung ausgibt.
  Einrückungen legst du durch Ziehen nach rechts fest. <br/>
  Feedback erhältst du über „Get Feedback“, einen Neustart über „Reset Problem“.
---

<div id="p1-trash" class="sortable-code"></div>
<div id="p1-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p1-feedback" value="Get Feedback"  type="button" />
  <input id="p1-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "name = input(\"Wie heißt du?\")\\n" +
    "print(\"Hallo, \" + name + \"!\")\\n" +
    "print(\"Auf Wiedersehen\")  #distractor\\n";

  var pp = new ParsonsWidget({
    sortableId: "p1-work",
    trashId:    "p1-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p1-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p1-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>
