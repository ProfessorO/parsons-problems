<div id="nested_ifs-sortableTrash" class="sortable-code"></div> 
<div id="nested_ifs-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="nested_ifs-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="nested_ifs-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "let x = 6;\n" +
    "if (x > 3)\n" +
    "	x -= 2;\n" +
    "if (x % 2 == 0) // even\n" +
    "	x++;\n" +
    "else\n" +
    "	if (x > 3)\n" +
    "    	x = 1;\n" +
    "console.log(x); // 5\n" +
    "x *= 2; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "nested_ifs-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#nested_ifs-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#nested_ifs-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
