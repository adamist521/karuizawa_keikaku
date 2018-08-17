<iframe src="https://calendar.google.com/calendar/embed?height=600&amp;wkst=1&amp;bgcolor=%23FFFFFF&amp;src=6ga0b959sghi4furfh0mqt1qgc%40group.calendar.google.com&amp;color=%236B3304&amp;ctz=Asia%2FTokyo" style="border-width:0" width="800" height="600" frameborder="0" scrolling="no"></iframe>



<script>
var urlToGetAllOpenBugs = "https://api.github.com/repos/jquery/jquery/issues?state=open&labels=bug";

$(document).ready(function () {
    $.getJSON(urlToGetAllOpenBugs, function (allIssues) {
        $("div").append("found " + allIssues.length + " issues</br>");
        $.each(allIssues, function (i, issue) {
            $("div")
                .append("<b>" + issue.number + " - " + issue.title + "</b></br>")
                .append("created at: " + issue.created_at + "</br>")
                .append(issue.body + "</br></br></br>");
        });
    });
});
</script>
