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

Sometimes input will be partially sanitized, requiring you to exploit specific commands, like `grep`

The password for level 11 is `U82q5TCMMQ9xuFoI3dYX61s7OZD9JKoK`