<h1> Web-intro </h1>

<img width="575" alt="image" src="https://user-images.githubusercontent.com/107073731/202763463-a148e820-1beb-4b1e-9069-536eda8f6612.png">

After entering the ip adress given when we start the challenge this is what we see:

<img width="1280" alt="1" src="https://user-images.githubusercontent.com/107073731/202763565-af1cc62c-3f65-44f4-9982-a74b364e5ba0.png">

Because there aren't many things happening let's look and see if there are any cookies.

<img width="1280" alt="image" src="https://user-images.githubusercontent.com/107073731/202764612-356ab17a-e74b-49cf-8c25-ca8f961a4e61.png">

It looks like a JSON web token so let's decode it using https://jwt.io/.
<img width="1028" alt="image" src="https://user-images.githubusercontent.com/107073731/202764890-2dab9121-aada-4487-b950-1b0641d374d1.png">
I wonder what happens if instead of "logged_in": false we have "logged_in": true. 
<img width="1280" alt="image" src="https://user-images.githubusercontent.com/107073731/202765167-aab06636-c398-443b-a858-03128d06c10d.png">
We see the site uses flask. If we search for flask we see we can use:
<p> flask-unsign --wordlist /usr/share/wordlists/rockyou.txt --unsign --cookie '<cookie>' --no-literal-eval to find the secret key </p>
  and then use this:
  <p> </p>
  <p> flask-unsign --sign --cookie "{'logged_in': True}" --secret 'CHANGEME' to sign the cookie to be logged in: true but with the secret key. </p>
<img width="853" alt="image" src="https://user-images.githubusercontent.com/107073731/202767204-982e15d1-0e73-46e0-9cfe-ce8a896b1460.png">
<p> We find this way that the secret key is password and now we change the cookie to logged in true using the key too  </p>
<img width="848" alt="image" src="https://user-images.githubusercontent.com/107073731/202767487-d5ab6494-a0a3-4e54-a033-93ddd8778db9.png">
<p> Now if we put this cookie instead of the default one in the site we get the flag when we reload the page. </p>
<img width="1279" alt="image" src="https://user-images.githubusercontent.com/107073731/202767671-a0912b25-c9a2-42fc-b481-646a4e45ee05.png">

