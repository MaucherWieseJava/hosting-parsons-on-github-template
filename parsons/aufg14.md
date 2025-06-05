---
layout: default
title: Puzzle 14 – Verzweigungen (Zahlen-Klassifikation) [2D]
description: >-
  Klassifiziere eine eingegebene Zahl als positiv/negativ und
  gerade/ungerade. Verwende verschachtelte if-Strukturen.
---

<div id="p14-trash" class="sortable-code"></div>
<div id="p14-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p14-feedback" value="Get Feedback"  type="button" />
  <input id="p14-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "zahl = int(input(\"Gib eine Zahl ein: \"))\n" +
    "if zahl > 0:\n" +
    "    print(\"Die Zahl ist positiv\")\n" +
    "    if zahl % 2 == 0:\n" +
    "        print(\"und gerade\")\n" +
    "    else:\n" +
    "        print(\"und ungerade\")\n" +
    "elif zahl < 0:\n" +
    "    print(\"Die Zahl ist negativ\")\n" +
    "else:\n" +
    "    print(\"Die Zahl ist null\")\n" +
    "print(\"Klassifikation beendet\")\n" +
    "if zahl == 0:  #distractor\n" +
    "print(\"Zahl ist positiv\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p14-work",
    trashId:    "p14-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p14-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p14-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg13.html) | [Next](./aufg15.html)
