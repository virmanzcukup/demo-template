<!DOCTYPE html>
<html>
<head>
<title></title> 
<link rel="icon" href="img/logo.png" />
<meta charset="utf-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge"> 
<meta http-equiv="X-UA-Compatible" content="chrome">
<meta name="viewport" content="width=device-width, user-scalable=no"> 
<meta http-equiv="pragma" content="no-cache"/>
<meta http-equiv="expires" content="-1"/>

<link href="css/bootstrap.css" rel="stylesheet">
<link href="css/animated.css" rel="stylesheet">
<link href="css/vinesa.css" rel="stylesheet">

</head>
<!--top border-->
<body style="margin-top:0px">
<div class="container">
<center>
<div class="warning animate__animated animate__backInUp">
<div class="warning-content">
<br>
<div class="notif-utama">

<b>Tidak ada koneksi</b>
</div>

<br>

<video autoplay loop controls id="vcnetVideo">
  <source src="int.mp4" type="video/mp4" />
</video>

<b>
Silahkan registrasi untuk mendapatkan koneksi internet<br>
atau lakukan pembayaran, agar koneksi tetap lancar</b>

<br>
<br>
<button class="tombol-warning" onclick="popClose();"><span class="glyphicon glyphicon-off"></span>  &nbsp;LOGIN </button>
<br>
<br>
</div>
</div>
</div>


<!--top border-->
<center>

<div class="col-md-6 col-md-offset-3 col-sm-0 col-sm-offset-2" style="padding:25px;">

<a href="registrasi.html">
	<button type="btn"  class="tombol-pay animate__animated animate__bounceInRight"><b>REGISTRASI</b></button></a>
<a data-toggle="collapse" href="#collapse1">
	<button type="btn"  class="tombol-pay animate__animated animate__bounceInLeft"><b>LOGIN</b></button></a>
	
<div id="collapse1" class="panel-collapse collapse ">
					<br>
<div class="tombol-pay animate__animated animate__flip" style="display:auto">
$(if error)<span class="blink"><b style="font-size:12px; color:red">Nomor pelanggan tidak sesuai silahkan coba kembali...!</b></span>$(endif)<br>
Silahkan Ketik ID pelanggan dan pastikan kodenya sesuai.
</div>
	
	<form autocomplete="off" name="login" action="$(link-login-only)" method="post" 
$(if chap-id) onSubmit="return doLogin()" $(endif) style="padding:5px;">
<input type="hidden" name="dst" value="$(link-orig)" />
<input type="hidden" name="popup" value="true" />

<input type="username" onkeyup="this.value = this.value.tolowercase();" 
 class="tombol-pay" name="username" value="$(username)" placeholder="ID Pelanggan" required /> 
 
<input type="hidden" onkeyup="this.value = this.value.tolowercase();" name="password" placeholder="PASSWORD" required /> 

<button class="tombol-pay" style="margin:5px" type="submit">
<b><span class="glyphicon glyphicon-off"></span>&nbsp; Aktifkan</b></button>
</form>
	
	
	
	</div>
<center>
	<img src="img/logo.png" style="width:100%; max-width:200px; height:150px;">
	

	<br>
	  <a href="aktivasi.html">
	  <button type="button" class="tombol-pay animate__animated animate__bounceInUp" ><b>CARA PEMBAYARAN</b></button></a>
</div>




















<style>.animasi-teks {
  font-size: 12px;
  width: 100%;
  white-space:nowrap;
  overflow:hidden;
  -webkit-animation: typing 5s steps(70, end);
  animation: animasi-ketik 5s steps(70, end);
}
@keyframes animasi-ketik{
  from { width: 0; }
}
@-webkit-keyframes animasi-ketik{
  from { width: 0; }
}</style>
  
$(if chap-id)
		<form name="sendin" action="$(link-login-only)" method="post">
			<input type="hidden" name="username" />
			<input type="hidden" name="password" />
			<input type="hidden" name="dst" value="$(link-orig)" />
			<input type="hidden" name="popup" value="true" />
		</form>
		<script type="text/javascript" src="md5.js"></script>
		<script type="text/javascript">
		<!--
			function doLogin() {
			document.sendin.username.value = document.login.username.value;
			document.sendin.password.value = hexMD5('$(chap-id)' + document.login.password.value + '$(chap-challenge)');
			document.sendin.submit();
			return false;
			}
		//-->
		</script>
		$(endif)
		

<script type="text/javascript">

    var username = document.login.username;
    var password = document.login.password;
    var luser = document.getElementById("luser");
    var lpass = document.getElementById("lpass");
    var btnmem = document.getElementById("btnmem");
    var btnvcr = document.getElementById("btnvcr");

    // set password = username
    function setpass() {
      var user = username.value
      password.value = user;
    }

    username.onkeyup = setpass;


    // change to voucher mode
    function voucher() {
      username.focus();
      username.onkeyup = setpass;
      username.placeholder = "KODE VOUCHER";
      password.type = "hidden";
      password.value = username.value;
    }

    // change to member mode
    function member() {
      username.focus();
      username.onkeyup = "";
      username.placeholder = "USERNAME";
      password.type = "PASSWORD";
      password.value = "";

    }

    //-->
  </script>
			
<script>
// Set modal
document.querySelector(".warning").style.opacity="1",
document.querySelector(".warning").style.display="block"
</script>
<script type="text/javascript">
function popClose(){document.querySelector(".warning").style.display="none";}
function popup(){document.querySelector(".warning").style.display="true";}
</script>
<script src="js/jquery.js" type="text/javascript"></script>
<script src="js/bootstrap.js" type="text/javascript"></script>
</body>
</html>
