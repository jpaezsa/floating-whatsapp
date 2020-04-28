# Shopify

1. Upload files to /Assets on Shopify theme

```
floating-wpp.min.css.liquid
floating-wpp.min.js.liquid
jquery-3.3.1.min.js.liquid
whatsapp.svg
```

2. Paste the next code on theme.liquid after star <body>
> Note: obtain url whatsapp.svg image and edit the script

```
<!-- OTRO -->
	{{ 'floating-wpp.min.js' | asset_url | script_tag }}
	{{ 'floating-wpp.min.css' | asset_url | stylesheet_tag }}
	{{ 'jquery-3.3.1.min.js' | asset_url | script_tag }}

	<!-- BTN -->
		<div class="WAbtn" style="{ z-index: 9999 !important; }">
			<div id="WAButton" ></div>
		</div>    
	<!-- BTN -->
    
 
	<script type="text/javascript">
		jQuery.noConflict(true);
		$(function () {
			$('#WAButton').floatingWhatsApp({
				phone: '52 1234567890 ', //WhatsApp Business phone number
				headerTitle: 'Chatea por WhatsApp!…', //Popup Title
				popupMessage: 'Hola, como podemos ayudarte?…', //Popup Message
				showPopup: true, //Enables popup display
				buttonImage: '<img src="https://cdn.shopify.com/s/files/1/0270/3533/6803/files/whatsapp.svg?v=1588027983" />', //Button Image
				//headerColor: 'crimson', //Custom header color
				//backgroundColor: 'crimson', //Custom background button color
				position: "right" //Position: left | right

			});
		});
	</script>
		
<!-- OTRO -->
````
