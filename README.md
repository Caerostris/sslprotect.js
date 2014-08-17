# sslprotect.js

sslprotect.js is a small javascript file which provides limited protection against tools like sslstrip.  
once the page has loaded, sslstrip checks if the used protocol is `https:`. If this is not the case, the user is redirected to a warning page.  
This tool can offer no real protection because it can be stripped out just as easily as the https:// tag.  
It's much rather a lame security through obscurity script and should not be relied on.  
sslprotect.js can also offer no protection to insecure sites with secure forms as the warning will appear after sensitive data has already been submitted.  
But: It's still better than nothing ;-)

# Usage
You can either include the sslprotect.js file

    <script type="text/javascript" src="/sslprotect.js"></script>

or include the three lines directly:

    <script type="text/javascript">
    	var a=String.fromCharCode(104, 116, 116, 112, 115, 58)
    	if(window.location.protocol!=a)
    		window.location = "http://caerostris.github.io/sslprotect.js"
    </script>

# License
sslprotect.js is release under the Mozzila Public License, v. 2.0