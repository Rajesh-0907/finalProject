                                                                                                
 $("#myBtn").click(function(){
        var str = $("#name").val();
        localStorage.clear();
        localStorage.setItem("name", str);


    });
 


