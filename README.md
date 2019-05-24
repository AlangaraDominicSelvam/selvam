<!DOCTYPE html>
<html>
	<head>
		<title>Dr.VIJAY BIRHDAY Countdown</title>
		<style type="text/css">
		body {
			background: #ff3988;
		}
 
		.countdownContainer{
			position: absolute;
			top: 50%;
			left: 50%;
			transform : translateX(-50%) translateY(-50%);
			text-align: center;
			background: #ddd;
			border: 1px solid #999;
			padding: 10px;
			box-shadow: 0 0 5px 3px #ccc;
			border-radius:10px;
		}
 
		.info {
			font-size: 80px;
		}
		#footer-copyright{font-family: Arial, Helvetica, sans-serif; left: 100%; background-color:blue; height:50px; color:#b1b1b1; clear:both}
        #copyright{font-family: Arial, Helvetica, sans-serif; padding:23px 0 0 0px; font-size:14px; text-align:center}
        #footer-copyright a, #footer-copyright a:visited{color:#b1b1b1}
		</style>
	</head>
	<body>
		<table class="countdownContainer">
			<tr class="info">
				<td colspan="4">Dr.VIJAY BIRTHDAY</td>
			</tr>
			<tr class="info">
				<td id="days">120</td>
				<td id="hours">4</td>
				<td id="minutes">12</td>
				<td id="seconds">12</td>
			</tr>
			<tr>
				<td>Days</td>
				<td>Hours</td>
				<td>Minutes</td>
				<td>Seconds</td>
			</tr>
		</table>

<div id="footer-copyright" style="border-radius:10px;">
        <div id="copyright">Designed by <a>HELMAN & DOMINIC</a></div>
    </div>


		<script type="text/javascript">
 
			function countdown(){
				var now = new Date();
				var eventDate = new Date(2019, 5, 23);
 
				var currentTiime = now.getTime();
				var eventTime = eventDate.getTime();
 
				var remTime = eventTime - currentTiime;
 
				var s = Math.floor(remTime / 1000);
				var m = Math.floor(s / 60);
				var h = Math.floor(m / 60);
				var d = Math.floor(h / 24);
 
				h %= 24;
				m %= 60;
				s %= 60;
 
				h = (h < 10) ? "0" + h : h;
				m = (m < 10) ? "0" + m : m;
				s = (s < 10) ? "0" + s : s;
 
				document.getElementById("days").textContent = d;
				document.getElementById("days").innerText = d;
 
				document.getElementById("hours").textContent = h;
				document.getElementById("minutes").textContent = m;
				document.getElementById("seconds").textContent = s;
 
				setTimeout(countdown, 1000);
			}
 
			countdown();
		</script>
	</body>
</html>
