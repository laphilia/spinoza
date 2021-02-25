---
title: 'jquery test'
---

 <meta charset = "utf-8">
      <title>jQuery UI Dialog functionality</title>
      <link href = "https://code.jquery.com/ui/1.10.4/themes/ui-lightness/jquery-ui.css"
         rel = "stylesheet">
      <script src = "https://code.jquery.com/jquery-1.10.2.js"></script>
      <script src = "https://code.jquery.com/ui/1.10.4/jquery-ui.js"></script>
      
      <!-- CSS -->
      <style>
         .ui-widget-header,.ui-state-default, ui-button {
            background:#b9cd6d;
            border: 1px solid #b9cd6d;
            color: #FFFFFF;
            font-weight: bold;
         }
      </style>
      
      <!-- Javascript -->
      <script type = "text/javascript">
         $(function() {
            $( "#dialog-7" ).dialog({
               autoOpen: false, 
               resize: function( event, ui ) {
                  $( this ).dialog( "option", "title",
	         ui.size.height + " x " + ui.size.width );
               }
            });
            $( "#opener-6" ).click(function() {
               $( "#dialog-7" ).dialog( "open" );
            });
         });
      </script>

   

      <div id = "dialog-7" title = "Dialog Title goes here..."
         >Resize this dialog to see the dialog co-ordinates in the title!</div>
      <button id = "opener-6">Open Dialog</button>