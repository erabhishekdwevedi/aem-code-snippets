```
<form method="POST" enctype="multipart/form-data" id="fileUploadForm">
    <input type="text" name="fileName"/><br/><br/>
    <input type="file" name="uploadFile"/><br/><br/>
    <input type="submit" value="Submit" id="submit"/>
</form>	

<h2> Result From Servlet Response</h2>
<div id="response"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>

<script type="text/javascript">
   
   $(document).ready(function () {

    $("#submit").click(function (event) {
    
        event.preventDefault();
        
        var form = $('#fileUploadForm')[0];
        var data = new FormData(form);
        
       $("#submit").prop("disabled", true);  //Disable Submit Button until Ajax response comes back

        $.ajax({
            type: "POST",
            enctype: 'multipart/form-data',
            url: "/bin/servletpath",
            data: data,
            processData: false,
            contentType: false,
            cache: false,
            timeout: 500000,

            success: function (data) {
            
                $("#response").html(data);
                $("#submit").prop("disabled", false);  // Enable Submit button
              },
            
            error: function (e) {
              	$("#response").html(e.responseText);
                 console.log("ERROR : ", e);
                 
            }
        });

    });

});
</script>

```
