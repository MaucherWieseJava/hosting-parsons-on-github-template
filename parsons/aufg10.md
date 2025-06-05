---
layout: default
title: Puzzle 10 – Verzweigungen (Passwort-Prüfung) [2D]
description: >-
  Erstelle ein Passwort-Prüfungssystem mit mehreren Bedingungen.
  Achte auf die korrekte Verschachtelung der if-Anweisungen.
---

<div id="p10-trash" class="sortable-code"></div>
<div id="p10-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p10-feedback" value="Get Feedback"  type="button" />
  <input id="p10-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "passwort = input(\"Passwort eingeben: \")\n" +
    "if len(passwort) >= 8:\n" +
    "    if any(c.isdigit() for c in passwort):\n" +
    "        print(\"Passwort akzeptiert!\")\n" +
    "    else:\n" +
    "        print(\"Passwort braucht mindestens eine Zahl\")\n" +
    "else:\n" +
    "    print(\"Passwort zu kurz (min. 8 Zeichen)\")\n" +
    "print(\"Prüfung beendet\")\n" +
    "if len(passwort) < 5:  #distractor\n" +
    "print(\"Passwort gespeichert\")  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p10-work",
    trashId:    "p10-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p10-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p10-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg9.html) | [Next](./aufg11.html)
