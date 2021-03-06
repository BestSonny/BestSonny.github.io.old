---
layout: page
#title: deadline
permalink: /deadline/
---

<html>
<head>
<title>Academic Deadlines Countdown Timer</title>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.10.6/moment.min.js"></script>
<script type="text/javascript">
// DATABASE
var deadlines= new Array();
/* add yours here
deadlines.push({
  venue: "",
  area: "",
  deadline: moment("2000-00-00 00:00:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
  //website: "",
  //approx: 1,
});
*/
deadlines.push({
  venue: "ICML",
  area: "Machine Learning",
  deadline: moment("2017-02-05 23:59:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://icml.cc/2017/",
});
deadlines.push({
  venue: "NIPS",
  area: "Machine Learning",
  deadline: moment("2016-05-20 16:00:00 -0800", "YYYY-MM-DD HH:mm:ss Z"),
  website: "https://nips.cc/Conferences/2017",
});
deadlines.push({
  venue: "AISTATS",
  area: "Machine Learning",
  deadline: moment("2016-10-09 23:59:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://www.aistats.org/",
  approx: 1,
});
deadlines.push({
  venue: "KDD",
  area: "Data Mining",
  deadline: moment("2016-02-20 23:59:00 -0800", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://www.kdd.org/kdd2016/",
});

deadlines.push({
  venue: "UAI",
  area: "Machine Learning",
  deadline: moment("2016-03-03 23:59:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
});
deadlines.push({
  venue: "CVPR",
  area: "Computer Vision",
  deadline: moment("2016-11-11 23:00:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://cvpr2017.thecvf.com/",
});
deadlines.push({
  venue: "IJCAI Abstract",
  area: "Machine Learning",
  deadline: moment("2016-02-19 23:59:00 -1200", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://ijcai-16.org/",
});
deadlines.push({
  venue: "IJCAI Full Paper",
  area: "Machine Learning",
  deadline: moment("2016-02-02 23:59:00 -1200", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://ijcai-16.org/",
});
deadlines.push({
  venue: "COLT",
  area: "Machine Learning",
  deadline: moment("2016-02-19 23:59:00 -1100", "YYYY-MM-DD HH:mm:ss Z"),
});
deadlines.push({
  venue: "ICLR Abstract",
  area: "Deep Learning",
  deadline: moment("2015-11-12 17:00:00 -0500", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://www.iclr.cc/doku.php",
});
deadlines.push({
  venue: "ICLR Full Paper",
  area: "Deep Learning",
  deadline: moment("2015-11-19 17:00:00 -0500", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://www.iclr.cc/doku.php",
});
deadlines.push({
  venue: "ECCV",
  area: "Computer Vision",
  deadline: moment("2016-03-14 00:00:00 +0000", "YYYY-MM-DD HH:mm:ss Z"),
  website: "http://www.eccv2016.org/",
});
// HELPER FUNCTIONS
var timeDescription = function(x) {  
  return x.format("MM/DD/YYYY h:mm:ss A");
}
var timeLeftDescription = function(t) {
  if(t<0) t=0;
  var tseconds = t / 1000;
  var seconds = Math.floor(tseconds) % 60;
  var tminutes = tseconds / 60;
  var minutes = Math.floor(tminutes) % 60;
  var thours = tminutes / 60;
  var hours = Math.floor(thours) % 24;
  var tdays = thours / 24;
  var days = Math.floor(tdays);
  return days + " days, " + hours + "h " + minutes + "m " + seconds + "s";
}
// Display function, called every second or so
function refreshDisplay() {
  var d = moment();
  $("#currtime").text("Current time: " + timeDescription(d));
  
  // calculate and display deadlines
  for(var i=0;i<deadlines.length;i++) {
    var dl= deadlines[i];
    var timeLeft= dl.deadline - d;
    
    warningString= "";
    if("approx" in dl) { warningString= "based on previous year!"; }
    prefix = "";
    suffix = "";
    if ("website" in dl) {
      prefix = "<a class=\"sd\" href=\"" + dl.website + "\">";
      suffix = "</a>";
    }
    
    $("#deadline" + i).html(
      prefix + "<div class=\"tld\">" + timeLeftDescription(timeLeft) + "</div>"
             + "<div class=\"vd\">" + dl.venue + "</div>"
             + "<div class=\"ad\">" + dl.area + "</div>"
             + "<div class=\"td\">Deadline: " + timeDescription(dl.deadline) + "</div>"
             + "<div class=\"wd\">" + warningString + "</div>"
             + suffix
    );
  }
}
// int main(){}
$(document).ready(function() {
  deadlines.sort(function(a, b) {
    return a.deadline - b.deadline;
  });
  // create divs for all deadlines and insert into DOM
  for(var i=0;i<deadlines.length;i++) {
    $("<div class=dd id=deadline" + i + "></div>").appendTo("div#deadlinesdiv");
    var divid= "#deadline" + i;
    
    $(divid).hide();
    $(divid).fadeIn(100*(i+1), function() { }); // create a nice fade in effect
  }
 
  // set up deadline timer to redraw
  setInterval(
    function(){ refreshDisplay(); },
    1000
  );
  
  // draw!
  refreshDisplay();
});
</script>

<style type="text/css">
/* Some resetting */
body {
  /*font-family: Verdana, Helvetica, sans-serif;
  font-size: 12px;
  */
  padding: 0;
  margin: 0;
  background-color: white;
  color: #222;
}
/* Main content div */
#surround {
  margin-left: auto;
  margin-right: auto;
  margin-top: 50px;
  width: 600px;
  background-color: white;
}
/* Div that contains all deadlines */
#deadlinesdiv {
}
#currtime {
  font-size: 14px;
}
#bottompart {
  text-align: center;
}
/* Page title */
h1 {
  display: inline;
  margin-right: 10px;
  font-size: 35px;
}
/* Maintained by @karpathy */
#signature {
  position: absolute;
  bottom: auto;
  right: 0;
  text-align: center;
  padding-bottom: 15px;
  padding-right: 30px;
  /*font-size: 14px;*/
}
/* The cells that contain each deadline */
.dd {
  padding: 10px;
  margin-bottom: 3px;  
  background-color: #EEE;
  border: 1px solid #DDD;
  cursor: pointer;
  position: relative;
}
.dd:hover {
  background-color: #DDD;
  border: 1px solid #AAA;
  cursor: default;
}
/* website */
a:link {
  color: black;
  text-decoration: none;
}
a:visited {
  color: black;
  text-decoration: none;
}
/* Time left description div */
.tld {
  float: right;
  font-size: 18px;
  font-weight: bold;
  margin-top: 16px;
}
/* Area description div */
.ad {
  font-family: monospace;
}
/* Time description div */
.td {
}
/* Venue description div */
.vd {
  font-weight: bold;
  font-size: 16px;
}
/* Warning div */
.wd {
  position: absolute;
  bottom: 10px;
  right: 8px;
  color: #700;
  font-size: 10px;
}
#musiclink a {
  color: #AAA;
  position: fixed;
  bottom: 30px;
  right: 30px;
}
</style>
</head>

<body>
  {% include head.html %}
  <div id="surround">
    <h1>Academic Countdown</h1>
    <div id="currtime"></div>
    <br /><br />
    <div id="deadlinesdiv"></div>
    <br />
    <div id="bottompart">
      <br />
      <br />
    </div>
    <div id="musiclink"><a href="https://youtu.be/9jK-NcRmVcw?t=1m56s" target="_blank">Music</a></div>
  </div>

</body>
</html>