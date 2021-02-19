# license-plate-detection-website-code
<!DOCTYPE html>
<html>

<head>
	<title>Interactive Parking Map </title>

</head>

<body id="page-top" class="index backgroundImage">
	<nav class="navbar navbar-default navbar-static-top">
		<div class="container">
			<div class="navbar-header page-scroll">
				<button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1">
					<span class="sr-only">Toggle navigation</span>
					<span class="icon-bar"></span>

				</button>
				<a class="navbar-brand" href="#page-top">Start</a>
			</div>

			<div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
				<ul class="nav navbar-nav navbar-right">
					<li class="hidden">
						<a href="#page-top"></a>
					</li>
					<li class="page-scroll">
						<a href="#parkraum">The Parking Space</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>


	<section id="parkraum">
		<div class="container">
			<div class="row contentDiv">
				<div class="page-header">
					<h1>Parking Space</h1>
				</div>
				<p class="lead">This is an interactive map.
					<hr>

					<div>
						<div class="form-group dropdown theme-dropdown clearfix">
							<form id="mapForm">
								<button id="getPositionButton" type="button" class="btn btn-sm btn-info" onclick="currentPosition();">Show Current Possition</button>
								<label for="selectParkzone">Select Parking zone: </label>
								<select id="selectParkzone" class="btn btn-sm">
									<select>
										<button id="resetButton" type="button" class="btn btn-sm btn-info" onclick="resetMap();">Reset to default</button>
							</form>
						</div>
						<div id="map" class="iframe-container"></div>
						<hr>

					</div>
			</div>
			<!-- /.row -->
		</div>
	</section>


	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css" integrity="sha384-rHyoN1iRsVXV4nD0JutlnGaslCJuC7uwjduW9SVrLvRYooPp2bWYgmgJQIXwl/Sp" crossorigin="anonymous">

	<script src="https://code.jquery.com/jquery-3.1.0.min.js" type="text/javascript"></script>

	<link rel="stylesheet" href="./css/custom.css">

	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.0.0-rc.3/dist/leaflet.css" />
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.6.3/css/font-awesome.min.css" />
	<script src="https://unpkg.com/leaflet@1.0.0-rc.3/dist/leaflet.js"></script>
	<script src="http://leaflet.github.io/Leaflet.label/leaflet.label.js"></script>
	<script src="./js/parkraum.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

	<script>
		$(document).ready(function() {
			initMap();
			placeZonesOnMap();
			loadScrolling();
			populateParkzoneDropdown();
		});
	</script>
