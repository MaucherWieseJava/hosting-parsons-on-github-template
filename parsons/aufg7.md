---
layout: default
title: Puzzle 7 – Schleifen (Countdown)
description: >-
  Erstelle einen Countdown von 5 bis 1 mit einer while-Schleife
  und gib am Ende "Start!" aus.
---

<div id="p7-trash" class="sortable-code"></div>
<div id="p7-work"  class="sortable-code"></div>
<div style="clear: both;"></div>

<p>
  <input id="p7-feedback" value="Get Feedback"  type="button" />
  <input id="p7-reset"    value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function () {
  var initial =
    "counter = 5\n" +
    "while counter > 0:\n" +
    "    print(counter)\n" +
    "    counter -= 1\n" +
    "print(\"Start!\")\n" +
    "counter += 1  #distractor\n" +
    "while counter < 10:  #distractor";

  var pp = new ParsonsWidget({
    sortableId: "p7-work",
    trashId:    "p7-trash",
    grader:     ParsonsWidget._graders.LineBasedGrader,
    can_indent: true,
    x_indent:   50,
    lang:       "en",
    max_wrong_lines: 10
  });
  pp.init(initial);
  pp.shuffleLines();
  $("#p7-reset").click(function (e) { e.preventDefault(); pp.shuffleLines(); });
  $("#p7-feedback").click(function (e) { e.preventDefault(); pp.getFeedback(); });
})();
</script>

[Previous](./aufg6.html) | [Next](./aufg8.html)
