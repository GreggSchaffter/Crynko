<p align="center">
  <img src ="/logo2.png?raw=true"/>
</p>

Crynko is a chrome extension that adds more security to your passwords on websites that users visit. It has become an issue where user data can not be completely trusted with the company that hosts the website(s) and your account. These issues range from passwords being stored as plain text on the website database to badly encrypted passwords. And when a hacker gets a hold of this data, your other accounts may be compromised because the same password is used. This is where Crynko comes in.

# How it works

Crynko, when a user registers a new account, will send a **pseudo-password** instead of the actual password. This pseudo-password will be . The pseudo-password is the password that gets encrypted and then hashed with an equation, which then is sent to the website database that contains the user's account. The pseudo-password will be encrypted using XOR cipher with a salt value and the string associated with the two-factor authentication question that is asked when the user creates the account; the result will be hashed using SHA256 hashing. If a malicious user obtains the pseudo-password instead of the actual password the website that was hacked will be the only site that has your pseudo-password rather than your actual password. All other accounts under Crynko will remain safe.

Because Crynko will be mainly a chrome extension, user data belonging to Crynko for a particular user can be synced and transfered to other browsers.

For more information on the inner workings of Crynko, look to the [documentation](https://github.com/GreggSchaffter/Crynko/blob/master/pdoc.pdf).

# Features
None

# Features to Implement
  * Modify password to pseudo password when user sends POST or GET request on registration
  * Storing URL and associated salt on Chrome local storage

# Future Plans
Obviously, not all users use Google Chrome for various reasons. Therefore, it is important to have the capability to expand the concept outside a single browser. One way to solve this issue is to make a background process that is able to do the samething as the Chrome extension. This version will most likely be done in C.

# Contribute
All contributions are accepted and encouraged. This means both the chrome extension, the concept and equations behind the project, and extending the project beyond the chrome extension.

# License
Crynko is under the [MIT license](https://opensource.org/licenses/MIT)
