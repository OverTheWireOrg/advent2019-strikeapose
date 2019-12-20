# Strike a pose

*The [OverTheWire Advent Bonanza 2019](https://advent2019.overthewire.org) challenge for Friday 20 December 2019*

Today is [Ugly Christmas Sweater
day](http://www.nationaluglychristmassweaterday.org/), a day when having a lack of style<br>is actually an advantage!

Today's challenge can yield two flags, because it has two independent parts.
You don't need to participate in both challenges, unless you want both flags.

### Part 1: Show us your ridiculous holiday outfit

Wearing your ~~ugliest~~ most awesome holiday outfit, recreate an iconic photo.
Use an image editor to place the original and the new image next to each other, like in the example Santa_outfit.jpg image.
Make sure your image does not exceed 640x480 and name it <teamname>_outfit.jpg.

### Part 2: Show us your heart

Although this holiday season is for many of us a happy occasion, let us<br>
not forget about all those that are less fortunate.

Contribute to any charity of your choosing, in any way that is helpful.<br>
Donating money is the easy way, but there are also a lot of other ways<br>
to help: donate clothes, toys, food, hugs or even your blood.<br><br>
Create a photo with some kind of evidence of your involvement, 
make sure your photo does not exceed 640x480 and name it <teamname>_heart.jpg.

### Submitting and rewards

- generate a public/private key pair that will later be used to send your reward to you. *KEEP THESE FILES SOMEWHERE*

```
openssl genrsa -out private.pem 2048
openssl rsa -in private.pem -outform PEM -pubout -out public.pem
```

- Create a pull request with both (or one of) the above pictures and mention your team name in the comment, and also paste your PUBLIC KEY there.
- now wait until we have a chance to merge your pull request.

- You reward will be sent to you in a comment of the pull request, encrypted with your public key.
To decrypt the encrypted message *reward.b64*, execute:
```
base64 -d <reward.b64 >reward.bin
openssl rsautl -decrypt -inkey private.pem -in reward.bin -out reward.txt
```

