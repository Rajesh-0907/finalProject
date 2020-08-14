var stri = window.localStorage.getItem("name");
$("#nam").text("welcome " + stri);

$("#restart").click(function(){location.reload();});

var clear = window.setInterval(comp,1000);
var sum = 0;
var sum1 = 0;
var sum2 = 0;
var sum3 = 0;
var sum4 = 0;
var color = ["red","blue","green","yellow","orange"];
var c1 = 0;
var c2 = 1;
var c3 = 2;
var c4 = 3;
var c5 = 4;
function change(){
    $("body").css("background-color", color[sum4]);
    $("#game").css("background-color", color[sum4]);

    ++sum4;
    if(sum4 > 4){
      sum4 = 0;
    }
    window.clearInterval(clear);
}
$("#red").click(function(){
  if(sum == 3){
    sum = 0;
  }
  ++sum;
  switch(sum){
  case 1:   $("#green").css("background-color", color[c4]);
            $("body").css("background-color", color[c4]);
            ++c4;

            if(c4 > 4)
            {c4 = 0;}
            break;

  case 2:   $("#orange").css("background-color", color[c1]);
            $("body").css("background-color", color[c1]);
            ++c1;
            if(c1 > 4)
            {c1 = 0;}
            break;

  case 3:   $("#red").css("background-color", color[c2]);
            $("body").css("background-color", color[c2]);
            ++c2;
            if(c2 > 4)
            {c2 = 0;}
            break;



  }


}
);


$("#blue").click(function(){
  if(sum1 == 2){
    sum1 = 0;
  }
  ++sum1;
  switch(sum1){
  case 1:   $("#yellow").css("background-color", color[c5]);
            $("body").css("background-color", color[c5]);
            ++c5;
            if(c5 > 4)
            {c5 = 0;}
            break;

  case 2:   $("#blue").css("background-color", color[c3]);
            $("body").css("background-color", color[c3]);
            ++c3;
            if(c3 > 4)
            {c3 = 0;}
            break;}
}
);

$("#green").click(function(){
  if(sum2 == 2){
    sum2 = 0;
  }
  ++sum2;
  switch(sum2){
  case 1:   $("#orange").css("background-color", color[c1]);
            $("body").css("background-color", color[c1]);
            ++c1;
            if(c1 > 4)
            {c1 = 0;}
            break;

  case 2:   $("#green").css("background-color", color[c4]);
            $("body").css("background-color", color[c4]);
            ++c4;
            if(c4 > 4)
            {c4 = 0;}
            break;}
}
);


$("#yellow").click(function(){
 $("#yellow").css("background-color", color[c5]);
 $("body").css("background-color", color[c5]);
 ++c5;
 if(c5 > 4)
 {c5 = 0;}
}
);

$("#orange").click(function(){
  if(sum3 == 2){
    sum3 = 0;
  }
  ++sum3;
  switch(sum3){
  case 1:   $("#green").css("background-color", color[c4]);
            $("body").css("background-color", color[c4]);
            ++c4;
            if(c4 > 4)
            {c4 = 0;}
            break;
    
   case 2:   $("#orange").css("background-color", color[c1]);
            $("body").css("background-color", color[c1]);
            ++c1;
            if(c1 > 4)
            {c1 = 0;}
            break;}
}
);
function comp(){
if(c1 == 3 && c2 == 3 && c3 == 3 && c4 == 3 && c5 == 3)
{ $("#orange").css("background-color", "black");
  $("#red").css("background-color", "black");
  $("#blue").css("background-color", "black");
  $("#green").css("background-color", "black");
  $("#yellow").css("background-color", "black");
  window.setInterval(change, 3000);

}
}


