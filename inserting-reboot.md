# Preparing Reboot integration.
To allow users to authorize your service, you can share the login link. You can place a link on your site or automatically redirect to the link to allow users to authorize it.

# Fetching user info
By using "Fetch user info from token"'s link, all you need to do is preform a GET request using that link. It should look something like this.
https://rebooted.link/getuserdetails.php?token=(user token here)&secret=(secret token here)

You must replace (secret token here) with your secret token for your application,, and (user token here) must be replaced with the the GET parameter userToken.
The server will return JSON with the user's 

- User ID, (id) (This will never change, so you can rely on that to identify a user)
- Username, (username)
- Email, (email)
- and Avatar. (avatar)

All info returned is a string. Avatar is a link, though.
You can handle this information how you need to in the backend.

# Congratulations!
Setup is complete.
