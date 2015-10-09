#Send Email By Javascript Example App
## https://medium.com/@hukenneth/send-an-email-using-only-javascript-40de8b9e6511

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