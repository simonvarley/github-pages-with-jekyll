<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie-edge">
	<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.2/Chart.min.js"></script>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
	<title>My Chart.js</title>
</head>	
<body>
	<div class="container">
			<canvas id="myChart"></canvas>
	</div>
	<script type="text/javascript">
		var myChart = document.getElementById('myChart').getContext('2d');

		// GLobal options
		Chart.defaults.global.defaultFontFamily = 'Arial';
		Chart.defaults.global.defaultFontSize = 18;
		Chart.defaults.global.defaultFontColor = '#777';

		var massPopChart = new Chart(myChart, {
			type: 'pie', //bar, horizontalBar, pie, line, doughnut, radar, polarArea
			data: {
				labels:['Boston', 'Worcester', ['Springfield', 'Is', 'a', 'very', 'long', 'city', 'name'], 'Lowell', 'Cambridge'],
				datasets:[{
					label:'Population',
					data:[617594,181045,153060, 106519,105162],
					//backgroundColor:'green'
					backgroundColor:[
						'rgba(255, 99, 132, 0.6)',
						'rgba(54, 162, 235, 0.6)',
						'rgba(255, 206, 86, 0.6)',
						'rgba(75,  192, 192, 0.6)',
						'rgba(153, 102, 255, 0.6)'
					],
					borderWidth:1,
					borderColor:'#777',
					hoverBorderWidth:3,
					hoverBorderColor:'#000'
				}]
			},
			options:{
				title:{
					display:true,
					text:'Largest Cities in MA',
					fontSize:25
				},
				legend:{
					display:true,	
					position:'right',
					labels:{
						fontColor:'#000'
					}
				},
				tooltips:{
					enabled:true
				}
			}
		});
	</script>

</body>
</html>
