---
layout: post
title: Running and Testing an IRC Bot Offline
---
Want to write an irc bot without getting kicked off your favorite server during
testing? Not to mention be able to play with it while offline&mdash;after all,
you shouldn't have to connect to the internet just to test your chat bot.
Recently I was recommended to use Charybdis to set up a local irc server for
testing. However, I quickly found a simpler solution, one that's more or
less plug-and-play, with minimal initial setup.

This article assumes a Linux-like operating system for specific instructions on
how to run certain commands, but it should be possible to use Mac OS X. As such,
some commands may vary.

Prompted by a <a href="http://blog.tremily.us/posts/Local_IRC_server/">Physics
student teacher's post about setting up a local IRC server for his students to
use</a>, I decided to look into <a href="http://ngircd.barton.de/">ngIRCd</a>.

Installation is easy enough:
{% highlight bash %}
apt-get install ngircd
{% endhighlight %}
(You may need to use 'sudo')

He goes into slightly more depth about configuring ngird, which you can do by
editting the configurations in /etc/ngircd/ngirdc.conf if you like; for
simple bot testing, I found this necessary. After installing, simply run
{% highlight bash %}
ngirdc
{% endhighlight %}
in a terminal to start it. It will look like nothing happened, but you will now
be able to connect to your local server using
{% highlight bash %}
irssi -c localhost
{% endhighlight %}
or whatever your favorite irc client is.

You can stop it at any time by calling
{% highlight bash %}
/etc/init.d/ngircd stop
{% endhighlight %}
I believe that it will run every time the box on which it's run is turned on
(meaning that shutting down or restarting will only stop ngIRCd while the box
is off), though I have not tested that extensively. You can tell if it is
running my executing
{% highlight bash %}
pidof ngircd
{% endhighlight %}
in a terminal. If it returns a pid (a number), then ngircd is running. You can
also use this number to kill the job, but there is no reason to do that instead
of the stop command above.

Now that the local IRC server is set up, you can use it to test your irc bot
by connecting it to localhost.

If you notice that your bot doesn't seem to be connecting and are extending
Twisted's irc.IRCClient, consider adding

{% highlight python %}
def dataReceived(self, bytes):
        print repr(bytes)
        return irc.IRCClient.dataReceived(self, bytes)
{% endhighlight %}

to your bot's code. This will let you see all the data your bot receives, and
may help with troubleshooting a bad connection. For example, when I first tried
to connect <a href="promptbot">Promptbot</a> to localhost, it never showed up in
the default channel, nor even on the local network. Once I added the above code,
I was able to see that it was getting the following message:
{% highlight bash %}
ERROR :Access denied: Bad password?
{% endhighlight %}
This happened because I had set <a href="promptbot">Promptbot</a> up with a
default nick and password. Since no password was configured for the server, it
was being rejected for even trying to use a password at all. Once I set the
default password to null, it was able to connect, and I was able to test my bot
to my heart's content.

Need help troubleshooting? Feel free to contact me! I'm always open for
questions... especially related to <a href="promptbot">Promptbot</a>/irc bots!
