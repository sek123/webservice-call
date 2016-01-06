# webservice-call
please i need help on calling webservice from phonegap. The code below keep displaying not working.

<!DOCTYPE html>
<html>
    <head>
        <title>jQM Complex Demo</title>
        <meta http-equiv='Content-Type' content='text/html; charset=utf-8'/>
        <meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; minimum-scale=1.0; user-scalable=no; target-densityDpi=device-dpi"/>
		       <script type="text/javascript" charset="utf-8" src="jqm/jquery-2.0.3.min.js"></script>  
        <link rel="stylesheet" href="jqm/jquery.mobile-1.4.0.min.css" />     
        <script type="text/javascript" charset="utf-8" src="jqm/jquery.mobile-1.4.0.min.js"></script> 		
        <script>
    $.ajax({
        type       : "POST",
        url        : "http://192.168.1.102/web/RayanWebService/RayanSevice.php",
        crossDomain: false,
        beforeSend : function() {$.mobile.loading('show')},
        complete   : function() {$.mobile.loading('hide')},
        data       : {name:'Sekinat',phoneNum:'08087718802',email: 'joke@gmail',password: 'joke'},
        dataType   : 'xml',
					
        success    : function(response) {
            //console.error(JSON.stringify(response));
            alert('Works!');
        },
        error      : function() {
            //console.error("error");
            alert('Not working!');                  
        }
    });     
        </script>
		
    </head>
    <body>
        <div data-role="page" id="index">
            <div data-theme="b" data-role="header">
                <h1>Index page</h1>
            </div>

            <div data-role="content">

            </div>
        </div>    
    </body>
</html>   
