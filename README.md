
<html>
<head><style type="text/css">
body{background:rgba(120,100,200,.8)}
.hidden{height:10px;
}

#hissalary,#basic,#house,#otrate,#otearn,#totalsalary{font-weight:bold;}

#name,#salary,#ot{background:rgba(0,30,80);
text-align:center;
color:white;
padding:05px;
display:flex;
margin-left:50px;
height:40px;
width:250px
}

#submit{
background:rgba(250,0,0,.5);
display:flex;
margin-left:140px;
margin-top:-15px;
font-size:17px

}

</style></head>

<body>


<form>
<input id="name" type="text" placeholder="Name">
<input id="salary" type="number" placeholder="Salary">
<input id="ot" type="number" placeholder="OT Hour">
<br>
<input id="submit" type="submit">
</form>
<div class="hidden"></div>
<div id="hissalary"></div>
<div id="basic"></div>
<div id="house"></div>
<div id="otrate"></div>
<div id="otearn"></div>
<div id="totalsalary"></div>

<script type="text/javascript">
var myname=document.getElementById("name");
var mysalary=document.getElementById("salary");
var myot=document.getElementById("ot");
var mysubmit=document.getElementById("submit")

mysubmit.addEventListener("click",function(event){
event.preventDefault();
if(myname.value===""||mysalary.value==="")
{alert("Input field can not empty")}


var name=myname.value;
var salary=mysalary.value;
var othour=myot.value

var sum1850=salary-1850;

var basic=sum1850/1.5;

var house=basic*.5

var otrate=basic/208*2

var otearn=otrate*othour

var totalsalary=salary*salary/salary+otearn+(200)

document.getElementById("hissalary").innerHTML=name+" per month salary is: "+Math.round(salary)
document.getElementById("basic").innerHTML="Basic is: "+Math.round(basic)
document.getElementById("house").innerHTML="House Rent is: "+Math.round(house)
document.getElementById("otrate").innerHTML="His OT rate is: "+Math.round(otrate)
document.getElementById("otearn").innerHTML="His OT earn is: "+Math.round(otearn)
document.getElementById("totalsalary").innerHTML="His total salary is: "+Math.round(totalsalary)

}
)

</script>
</body></html>
