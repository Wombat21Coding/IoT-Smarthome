<!DOCTYPE html>
<html lang="de">
	<head>
		<title>IoT-Smarthome</title>
		<meta charset="UTF-8">
		<meta name="description" content="Control-Panel IoT-Smarthome">
		<meta name="author" content="Jan Schlich & Julian Bruyers">
		<meta name="keywords" content="IoT-Smarthome;Geue;Jan Schlich;Julian Bruyers">
		<meta name="thc_gehalt" content="696%">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
	</head>
		
	<body>
		<style>
			body{
				margin: 0;
				background-color:#808080;
				/*background-color:#ffffff;*/
			}
			
			.header{
				color: white;
				text-align: center;
				font-family: 'Consolas';
				font-weight: bold;
				font-size: 45px;
				margin-top: 0px;
				background-color: black;
				padding: 20px;
				text-decoration: none;
			
			}
			
			.footer {
				position: fixed;
				left: 0;
				bottom: 0;
				width: 100%;
				background-color: black;
				color: white;
				text-align: center;
				font-size: 20px;
			}
			.table{
				color: white;
				/*color: black;*/
				text-align: left;
				font-family: 'Lucida Console';
				font-size: 25px;
				margin-top: 0px;
				margin: auto;
				padding: 15px;
				text-decoration: none;
				border: 2px solid black;
				border-collapse: collapse;
			}
			
			.table table, th, td {
				border: 0px solid black; /* Auskommentieren: Rasteransicht*/
				border-collapse: collapse;
				border-spacing: 15px;
			}
			
			th, td {
				padding: 15px;
			}
			
			.table_centered{
				margin: auto;
			}
			
			.right{
				text-align: right;
			}
			
			.button_table {
				color: white;
				text-align: left;
				margin-top: 0px;
				margin-left: auto;
				margin-right: auto;
			}	
			
			.button_table button{
				color: black; 
				cursor: pointer; 			
				font-family: 'Consolas';
				font-size: 35px;
				border: 5px solid black;
				border-radius: 15px;		
			}
		
			.button_table button:hover {
				background-color: #888a8c;
			}
			
			.button_table button:active{
				transform: translate(4px,4px);
				box-shadow: 0 5px #666;
				transform: scale(1.02,1.02);
			}
			
			.button_table td{
				border: 0px solid black;
			}
			
			.on{
				background-color: #05b531;
			}
			
			.off{
				background-color: #b50505;
			}
			
		</style>
		<section>
			<div class="header">IoT-Smarthome Control-Panel</div>
			<br></br>
		</section>
		<section>
			<div class="table">
				 <table style="width:auto; align: center;" class="table_centered">
					<tr>
						<th style="font-weight: bold;">Sensor&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th>
						<th class="right" style="font-weight: bold;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Wert</th>
					</tr>
					<tr>
						<td>Temperatur</td>
						<td class="right">
						temperature
						°C</td>
					</tr>
					<tr>
						<td>Luftfeuchtigkeit</td>
						<td class="right">
						humidity
						%</td>
					</tr>
					<tr>
						<td>Brennbare Gase</td>
						<td class="right">
						gas_lpg
						ppP</td>
					</tr>
					<tr>
						<td>Kohlenstoffmonoxid</td>
						<td class="right">
						gas_co
						ppP</td>
					</tr>
					<tr>
						<td>Rauch</td>
						<td class="right">
						gas_smoke
						ppP</td>
					</tr>
				</table> 
			</div>
		</section>
		<section>
			<table style = "width: auto; align: center;" class="button_table">
				<tr>
					<td><a href=\"/led1"><button class="on">LED | 1&nbsp</button></a></td>
					
					<td><a href=\"/led2"><button class="on">LED | 2&nbsp</button></a></td>
				</tr>
			</table>
		</section>
		<section>
			<div class="footer">
				<p>By: Jan Schlich, Julian Bruyers</p>
			</div>
		</section>
	</body>
</html>

<script>
	function redirect(){
		window.location = 'http://192.168.4.1';
	}
	function reloadPage(){
		window.location = 'http://192.168.4.1';
	}
	setTimeout(reloadPage, 
	refresh_controlpanel
	)
</script>
