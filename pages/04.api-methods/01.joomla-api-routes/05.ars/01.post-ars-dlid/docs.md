---
title: 'POST ars/dlid'
taxonomy:
    category:
        - docs
---

Facilitates secure AJAX update of Akeeba Release System download ID for websites where cAPI is installed. This allows cAPI Core and extensions to properly authenticate against the repository server when looking for and attempting to download updates via Joomla Updater.

This is a limited use-case method because, right now, it is only implemented within the cAPI options view. It relies on a unique nonce, based off the Joomla sessions, to ensure the request to update the DLID (Akeeba Release System Download ID) comes from an authorized source. It also requires a Super Admin Joomla session. Also note that because the DLID is passed through the HTTP header, it is not subject to logging by Apache (or other web server log tools). *** Always secure your Joomla backend with HTTPS. ***

Beyond just updating the DLID, this method showcases a proof-of-concept for developing a secure method for implementing browser-based AJAX calls to the web server (although there much more work to be done on this concept, overall).

### Resource URL
https://yourdomain.com/api/v1/ars/dlid

### Resource Information

| Option | Description |
| ------ | ----------- |
| Request format	|	Request Header Parameter	|
| Response formats   | JSON |
| Requires authentication | Optional, session-based - Response depends on Joomla content security and user permissions levels. |
| Rate limited    | NO |

### Request Header Parameters

|  key  |  Details  |  
|  :-----          |  :-----          |
|  **dlid** | <ul><li>required</li><li>numeric</li></ul> |


### Example Request

POST
https://yourdomain.com/api/v1/ars/dlid

### Example Result

#### JSON Response

A successful response will return message:

* Code:		200
* Message:	"Download ID update successful."

#### Response Headers

(see above)

### Additional Information

Since this method only has a single intended use case, documentation is not provided for other uses, although it is certainly a possiblity.

For those interested, this is the javascript required to faciliate the AJAX update of the DLID field in the Services Control Panel Options page.

#### Javascript
``` js
jQuery(document).ready(function(){
            jQuery('#jform_downloadid').on('change', function() {
                jQuery.dlid = this.value
                    jQuery.ajax({
                        url: 'https://yourdomain.com/api/v1/ars/dlid',
                        type: 'POST',
                        beforeSend: function(xhr){
                        xhr.setRequestHeader('nonce', 'WW91IGp1c3QgaGFkIHRvIGRlY29kZSB0aGlzLCBkaWRuJ3QgeW91Pw==' );
                        xhr.setRequestHeader('dlid', jQuery.dlid );
                        },
                        success: function () {
                    },
                        error: function (xhr, textStatus, errorThrown) {
                        alert(xhr.status);
                    },
                        timeout: 120000
                    });

            });
        });
```
#### HTML
``` html
<input type="text" id="jform_downloadid" name="jform[downloadid]" size="30">
```