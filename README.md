# Tips-Js

![alt tag](http://i.imgur.com/dSkU3uC.png)

## disable right click on my web page, disable view source, disable developer tools
``` bash
<script language="javascript">
    window.oncontextmenu = function () { return false; };
    document.onkeydown = function(e){ if(event.keyCode == 123) {return false; } if(e.ctrlKey && e.shiftKey && e.keyCode == 'I'.charCodeAt(0)){return false;}if(e.ctrlKey && e.shiftKey && e.keyCode == 'J'.charCodeAt(0)){return false;}if(e.ctrlKey && e.keyCode == 'U'.charCodeAt(0)){return false;}}
</script>
```

## Automatically  Refresh DOM HTML
``` bash
<div id="re"></div>

<script type="text/javascript">
    setInterval(function () {
        $('#re').load(document.URL + ' #re');                  //Refresh 1 second
    }, 1000)
</script>
```

