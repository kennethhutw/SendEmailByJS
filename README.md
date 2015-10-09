#Send Email By Javascript Example App


/*
	** Send Email By Javascript Example App
	** Licensed under the Apache License v2.0
	** http://www.apache.org/licenses/LICENSE-2.0
	** Built by Kenneth Hu (Kenneth_hu@hotmail.com)
	** Get API KEY from https://mandrillapp.com/
	*/
$.ajax({
						  type: 'POST',
						  url: 'https://mandrillapp.com/api/1.0/messages/send.json',
						  data: {
							'key': 'YOUR API KEY HERE',
							'message': {
							  'from_email': 'kenneth_hu@livemail.tw',
							  'to': [
								  {
									'email': 'RECIPIENT_1@EMAIL.HERE',
									'name': 'RECIPIENT NAME (OPTIONAL)',
									'type': 'to'
								  },
								  {
									'email': 'RECIPIENT_2@EMAIL.HERE',
									'name': 'ANOTHER RECIPIENT NAME (OPTIONAL)',
									'type': 'to'
								  }
								],
							  'autotext': 'true',
							  'subject': 'YOUR SUBJECT HERE!',
							  'html': 'YOUR EMAIL CONTENT HERE! YOU CAN USE HTML!'
							}
						  }
					}).done(function(response) {
					   console.log(response); 
					});