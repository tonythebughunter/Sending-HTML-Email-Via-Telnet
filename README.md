# Sending-HTML-Email-Via-Telnet
HOW TO SEND HTML EMAIL USING SMTP PROTOCOL VIA TELNET
## First Connect to the mail server
    telnet localhost 25
In my case i used localhost with sendmail installed. You can scrap shodan for mail servers with open relays "port:25 open relay"
## Greet the server
    helo test
## Set Email Sender (This can spoof any email, Even which you don't have access to"
    mail from:<test@fakemail.com>
## Set Email Receiver
    rcpt to:<recp@victim.com>
## Start writting mail command
    data
## Subject
    Subject: <Urgent Notice>
## Content-Type (to write custom email format)
    Content-Type: text/html
## The body of the email
    <html><body><p>Hello, <a href='http://attacker.com'>Sign Up</a> for free coupon</p></body></html>
## End email body
    .
## Quit
    quit
