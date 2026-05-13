<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PORT SMS Generator</title>

<style>
    body{
        font-family: Arial, sans-serif;
        text-align:center;
        margin-top:50px;
    }

    input{
        padding:10px;
        width:250px;
        font-size:18px;
        margin-bottom:20px;
    }

    button{
        padding:12px 25px;
        font-size:18px;
        cursor:pointer;
    }
</style>
</head>

<body>

<h2>Send PORT SMS</h2>

<input type="text" id="mobile" placeholder="Enter Mobile Number">

<br>

<button onclick="sendSMS()">Send SMS</button>

<script>
function sendSMS() {

    let number = document.getElementById("mobile").value;

    if(number.length != 10){
        alert("Enter a valid 10 digit mobile number");
        return;
    }

    let message = "PORT " + number;

    window.location.href =
    "sms:1900?body=" + encodeURIComponent(message);
}
</script>

</body>
</html>
