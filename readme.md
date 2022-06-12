# Note-Share-App
It's the project that I developed with my 2 - member internship team in the internship program.

![](https://s8.gifyu.com/images/note-share.gif)
# What's this?
It is a Web Based Application in which helps you create and organize digital notes—and keeps them in your personal account. Programmed with Python language that uses Flask and SQLite in Linux operating system.

### You can make the server publicly
```
app.run(host='0.0.0.0', port=8000)

```
### Autosave code
```
var timeoutId;
$('#content').on('input propertychange change', function() {
  clearTimeout(timeoutId);
  timeoutId = setTimeout(function() {
    var text = $("#content");
    {% if context.note %}
      $.ajax({
      type: "POST",
      url: "{{ url_for('edit',note_id=context.note.id) }}",
      data: text,
      });
    {% endif %}
    },1000);
  });
```
### Markdown Filter
```
#Import Python file
from flaskext.markdown import Markdown
markdown = Markdown(app)

#Import HTML file
{{note.content|markdown}}
```
