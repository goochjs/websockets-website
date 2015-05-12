# websockets-website

A simple [Apache-hosted][apache] website to test websockets connection to an [MQTT broker][mosquitto].  Pulled together in support of questions on [my blog post][blog].

These files set up a websockets client, which expects to connect to a MQTT v1.4 broker on *localhost* port 9001.  This can be changed in the file `index.html`.

Add the site to your instance of Apache then [*inspect*][inspect] the site in [Chrome][chrome] and look for traffic coming and going in the *Console* window.

You can also run a subscriber against your Mosquitto broker and see the messages coming back from the test site:

    mosquitto_sub -h localhost -t "#" -v -i commandlinesubscriber


[apache]: https://httpd.apache.org/
[mosquitto]: http://mosquitto.org/
[blog]: http://goochgooch.co.uk/2014/08/01/building-mosquitto-1-4/
[inspect]: http://superuser.com/questions/4640/what-is-the-inspect-element-feature-in-google-chrome
[chrome]: http://www.google.com/chrome/
