#Boxcar.io API library for CodeIgniter  
A CodeIgniter library that is a simple port of the Boxcar Provider PHP SDK

##Install
Install the library using sparks

	$ php tools/spark install boxcar


##Usage
In your controller simply load the library, set your login info, and call the API  
   
	$this->load->library('boxcar');

	//authentication details
	$this->boxcar->init('yourKey', 'yourSecret', 'http://store.ukd1.co.uk.s3.amazonaws.com/ukd1_small.png');

	// send a broadcast (to all your subscribers)
	$brodcast = $this->boxcar->broadcast('Test Name', 'Test Broadcast, this was sent at ' . date('r'));

	var_dump($broadcast);


See [the Boxcar Provider API documentation](http://boxcar.io/help/api/providers) for API details.

Library created by [Ben Edmunds](http://benedmunds.com).