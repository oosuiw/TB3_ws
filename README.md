# TB3_ws
This is the full archive of the workspace built on ubunt22.04 , ROS2 humble.   

Uploaded because the build took a long time due to low memory.  

Repository cloning is recommended for the following people,  

1. whose builds are not progressing by more than 28% in 5 hours due to low memory
2. cannot swap memory due to insufficient storage

| RasPi                | Micro SD                 | BUILD     |  
|----------------------|----------------------|----------------------|
| RasPi3                  | 16Gib                   | X      | 
| RasPi3                  | 256Gib                   | X       | 
| RasPi4                  | 256Gib                   | O       |

**Version built on RasPi4 and 256Gibs is now available!**

*USB Keyboard is working!*
<pre>
<code id="code-block">
def hello_world():
    print("Hello, world!")
</code>
</pre>
<button onclick="copyToClipboard()">Copy</button>

<script>
function copyToClipboard() {
    var code = document.getElementById("code-block").innerText;
    navigator.clipboard.writeText(code).then(function() {
        alert("Copied to clipboard!");
    }, function(err) {
        alert("Failed to copy: ", err);
    });
}
</script>
