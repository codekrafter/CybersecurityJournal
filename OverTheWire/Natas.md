# Natas - Web Vulnerabilities

## Level 0 - Inspect Element

You can open inspect element in chrome to find hidden HTML elements.

The password for level 1 is: `gtVrDuiDfck831PqWsLEZy5gyDz1clto`

## Level 1 - Alternative Ways of Viewing Page Source

Sometimes right clicking can be not possible/blocked. You can view the HTML source by opening it with keybinds or directly viewing the HTML source.

The password for level 2 is `ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi`

## Level 2 - Forceful Browsing

By exploring resources displayed on webpages, you can find directorys. By visiting directories directly (ex. `files/`) you can find all resources in the directory.

The password for level 3 is `sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14`

## Level 3 - Robots.txt

By visiting the `robots.txt` of the domain, you can find paths that are hidden from search engines/web crawlers.

The password for level 4 is `Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ`

## Level 4 - Command Line Utilities/Headers

Sometimes web pages will adjust their content based on HTTP headers. These are not always controllable in a web browser, but are almost always able to be set through a command line utility, like cURL.

The password for level 5 is `iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq`

## Level 5 - Cookies and Local Storage

Applications will sometimes read cookies/local storage in the browser to check authentication. If they read a boolean value then you can manipulate that to fake authentication. Secure apps will instead rely on a token only on the client-side.

The pasword for level 6 is `aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1`

## Level 6 - Infering Hidden Values from Server-side Code

If you gain access to the server-side code you can more easily infilitrate web applications. You can read the code and find secret values that can be used to gain access to private information.

The password for level 7 is `7z3hEENjQtflzgnT29q7wAvMNfZdh0i9`

## Level 7 - Un-sanitized Server-side File Reads

Some applications will dynamically read files from the server based on a user-inputted string. If this is not properly sanitized/validated then it can be exploited to read private values from the server.

The password for level 8 is `DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe`

## Level 8 - Decoding Values

Sometimes values with be passed through encoding functions to obscure values. If you figure out the functions you can use the inverse to get the secret values.

The password for level 9 is `W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl`

## Level 9 - Executing client-side strings

Sometimes applications will run commands that pass in user-side strings as arguments. Discovering this allows it to be exploited, as users can append unauthorized commands to execute malicous code on the server.

The password for level 10 is `nOpp1igQAkUzaI1GUUjzn1bFVj7xCNzu`

## Level 10 - Exploiting Specific Commands

Sometimes input will be partially sanitized, requiring you to exploit specific commands, like `grep`. For this challenge any input containing "&", "|", ":" was declared invalid, so it was impossible to execute additional commands in the remote enviroment. This instead required using a single letter as a filter value, and passing the file that contains the next level's password to the end of the filter, thus passing it to `grep` as another file to search. If the password contained the guessed letter, than it will show up at the bottom of the found lines.

The password for level 11 is `U82q5TCMMQ9xuFoI3dYX61s7OZD9JKoK`

## Level 11 - Weak Encryption

Sometimes data will be encrypted using methods that have known vulnerabilities. This can be exploited to modify sensitive application data. For this activity the application stores a background color, and a value for if the password should be shown. This is encoded in a JSON format, ran through XOR encryption and then base64 encoded. XOR encryption has a known vulnerability that can be exploited to find the key if you have the ciphertext and plaintext. This was exploited to find the key, and reencode data that enables the display of the password

The password for level 12 is `EDXp0pS26wLKHZy1rDBPUZk0RKfLGIR3`

## Level 12 - Remote Code Execution/Executable Disguising

Someones files that contain executable code can be disgused as another type of file. This can be used to execute malicous code on a server/PC. This level features an uploader that accepts any jpg. The extension is enforced as `.jpg`, although the file that the jpg will be stored as is stored in a `<input type="hidden"/>` on the page. It defaults to random `.jpg` file, but if you change that to a `.php` extension and upload a file that contains PHP code as a `.jpg`, then you can end up with custom PHP code on the server. That code can simply echo the password file, which gives the password for the next level.

The password for level 13 is `jmLTY0qiPZBbaKc9341cqPQZBJv7MQbY`

## Level 13 - Magic Bytes

How applications can determine file types (most of the time) is by reading the first few bytes of the file, and check to see if they match the file type's "magic bytes". This allows for easy file type detection, but is open to exploits. In this level the uploaded file is verified to be an image by checking magic bytes. That can be bypassed by putting the magic bytes for a JPEG file before our PHP code.

The password for level 14 is `Lg96M10TdfaPyVBkJdjymbllQ5L6qdl1`

## Level 14 - SQL Injection

Some applications will perform database queries using user data. This level attempts to find a row inside the users table that matches the given username and password. Passing `" or ""="` for both user name and password bypasses this, faking access.

The password for level 15 is `AwWj0w5cvxrZiONgZ9J5stNVkmxdk39J`