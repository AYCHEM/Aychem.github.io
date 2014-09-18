Subject: Frequently Asked Questions
Format: html

<div id="faq">
<script type="text/javascript">
$(document).ready(function() {

  $('#faq-search').show();
  $('#toc').hide();
  $('li.faq-item p').hide();

  var options = {
    valueNames: [ 'faq-section', 'faq-title' ]
  };
  
  var questionList = new List('faq', options);

	$('#filter-category').change(function() {			
		var category = $(this).val().toString();

		if (category == 'none') {
	        questionList.filter();
	    }
	    else {
	        questionList.filter(function(item) {
	            if (item.values().question_category == category) {
	                return true;
	            }
	            else {
	                return false;
	            }
	        });
	    }
        return false;		
  	});
  	
  	$(document).on('click', 'li.faq-item', function() {
      $(this).data('state', 'open').addClass('open');
      $(this).find('p').fadeIn();
  	});

});
</script>

<h1 class="text-center">Frequently Asked Questions</h1>

<div class="text-center">
  <input id="faq-search" class="search" placeholder="Search Questions">
</div>
<div id="toc">
<ul><li><a href="#about">What is Mailpile?</a><ul>
<li class="section-about"><a href="#about-1">What is Mailpile?</a></li>
<li class="section-about"><a href="#about-2">Where does Mailpile store my mail?</a></li>
<li class="section-about"><a href="#about-3">Then how do I access it when my computer is turned off?</a></li>
<li class="section-about"><a href="#about-4">Is Mailpile webmail like Gmail, Yahoo, Hotmail?</a></li>
<li class="section-about"><a href="#about-5">If I use Gmail, Yahoo, Hotmail with my Mailpile isn't my mail still going through their servers and kept there indefinitely?</a></li>
<li class="section-about"><a href="#about-6">How much does Mailpile cost?</a></li>
<li class="section-about"><a href="#about-7">I am a techie, can I change how Mailpile works?</a></li>
<li class="section-about"><a href="#about-8">If anyone can view the code &amp; change Mailpile, doesn't that make it less secure?</a></li>
</ul></li>
<li><a href="#basic">Basic Questions?</a><ul>
<li class="section-basic"><a href="#basic-1">What is Mailpile? Is it an email service?</a></li>
<li class="section-basic"><a href="#basic-2">Is Mailpile real?</a></li>
<li class="section-basic"><a href="#basic-3">Is Mailpile ready yet?</a></li>
<li class="section-basic"><a href="#basic-4">Can we use Mailpile as the standard mail solution for our clients/company/server?</a></li>
<li class="section-basic"><a href="#basic-5">How can I get a MailPile account?</a></li>
<li class="section-basic"><a href="#basic-6">Can I get a cool @mailpile.is email address?</a></li>
<li class="section-basic"><a href="#basic-7">Can I still Donate?</a></li>
<li class="section-basic"><a href="#basic-8">Is Mailpile always going to be free?</a></li>
<li class="section-basic"><a href="#basic-9">Is there a mailing list so I can follow on your work?</a></li>
<li class="section-basic"><a href="#basic-10">How do I get updates about your project?</a></li>
<li class="section-basic"><a href="#basic-11">Regarding accessibility, what happens when my computer is offline?</a></li>
</ul></li>
<li><a href="#look">Branding and Design</a><ul>
<li class="section-look"><a href="#look-1">Does Mailpile allow me to customize my install with a company logo, colors, font?</a></li>
<li class="section-look"><a href="#look-2">You used bad words in your video and I didn't like it.</a></li>
<li class="section-look"><a href="#look-3">I don't like your design, logo, font, layout, haircut.</a></li>
<li class="section-look"><a href="#look-4">I really liked your design, logo, font, layout, haircut.</a></li>
<li class="section-look"><a href="#look-5">Why didn't you use a more modern color palate?</a></li>
<li class="section-look"><a href="#look-6">Your font looks a bit fuzzy in my browser</a></li>
</ul></li>
<li><a href="#usability">Interface and Usability Design</a><ul>
<li class="section-usability"><a href="#usability-1">Will there be Open Source Smileys/Emoticons available in Mailpile?</a></li>
<li class="section-usability"><a href="#usability-2">Do you have any plans to implement threaded conversations, like gmail?</a></li>
<li class="section-usability"><a href="#usability-3">How do we make it easy enough for our elders to use?</a></li>
<li class="section-usability"><a href="#usability-4">Will there be any similarities to Eudora?</a></li>
<li class="section-usability"><a href="#usability-5">I don't find many programs that exist well in both the Windows and the Mac worlds. How do you plan to deliver this experience?</a></li>
<li class="section-usability"><a href="#usability-6">PGP encryption should be made simple. Does Mailpile's interface do this?</a></li>
<li class="section-usability"><a href="#usability-7">Will Mailpile inform users if an email they received was encrypted or not?</a></li>
<li class="section-usability"><a href="#usability-8">Will the composing interface make it easy to choose whether I want to encrypt or not encrypt an email?</a></li>
<li class="section-usability"><a href="#usability-9">Is installing Mailpile going to be a simple double-click icon that once installed just opens a browser and loads Mailpile?</a></li>
<li class="section-usability"><a href="#usability-10">Why isn't there more access to PGP encryption via the web interface?</a></li>
<li class="section-usability"><a href="#usability-11">I do not want automatically grouped conversations. I cannot track this way. Does your program do that too?</a></li>
<li class="section-usability"><a href="#usability-12">I love your mail client do you know its cpanel ready?</a></li>
</ul></li>
<li><a href="#crypto">Encryption and Security</a><ul>
<li class="section-crypto"><a href="#crypto-1">Is Mailpile an encrypted email service?</a></li>
<li class="section-crypto"><a href="#crypto-2">What is your PGP public key?</a></li>
<li class="section-crypto"><a href="#crypto-3">Can you please include <em>insert-some-random-encrypted-service</em>.</a></li>
<li class="section-crypto"><a href="#crypto-4">I was looking for a private email server that can hide my email address from everyone that I haven't mailed to, does your service provide this?</a></li>
<li class="section-crypto"><a href="#crypto-5">Is  it possible to delete a message that you send to someone, but you don't want them to keep in their account after certain period? (If not it should be developed).</a></li>
<li class="section-crypto"><a href="#crypto-6">Can you create a pseudonym email address that only the recipient can see to identify us and send us message to, but it does not reveal my actual email address?</a></li>
<li class="section-crypto"><a href="#crypto-7">How will you prevent governments from accessing your user database?</a></li>
<li class="section-crypto"><a href="#crypto-8">How safe is it to store email metadata in RAM (Random-access memory)?</a></li>
<li class="section-crypto"><a href="#crypto-9">Will it, by default, deploy using encrypted configuration data?</a></li>
<li class="section-crypto"><a href="#crypto-10">Would it possible to add support for one-time passwords?</a></li>
<li class="section-crypto"><a href="#crypto-11">How secure is the database? Is it stored on an encrypted volume?</a></li>
<li class="section-crypto"><a href="#crypto-12">How are attachments stored? Are they encrypted, as well?</a></li>
<li class="section-crypto"><a href="#crypto-13">Will search work with encrypted files? Or, are they residing on some encrypted file system, and seem un-encrypted to it?</a></li>
<li class="section-crypto"><a href="#crypto-14">Does Mailpile have no weak points when it comes to privacy/security? How can they be closed?</a></li>
<li class="section-crypto"><a href="#crypto-15">The decrypted message is vulnerable/visible on compromised system? Can it be obfuscated?</a></li>
<li class="section-crypto"><a href="#crypto-16">Will Mailpile work with .onion (Tor) domains?</a></li>
<li class="section-crypto"><a href="#crypto-17">Will it work when residing on an in-Tor server?</a></li>
<li class="section-crypto"><a href="#crypto-18">Will Mailpile support address aliases for incoming mail? (132txche6763fhjf@domain.onion = green_leaf_dude@domain.onion)</a></li>
<li class="section-crypto"><a href="#crypto-19">Isn't email forwarding a possible breach of security?</a></li>
<li class="section-crypto"><a href="#crypto-20">How will this service compare with something like Hushmail which claims to offer message en/decryption in browser as well as IMAP (if one pays).</a></li>
<li class="section-crypto"><a href="#crypto-21">Is MailPile a viable non-centralized solution to issues like those faced by other privacy focused email companies like Lavabit or Silent Circle?</a></li>
<li class="section-crypto"><a href="#crypto-22">What happens when you are communicating with people who are still hosted by Google or a self hosted insecure server? Do they need to implement something too?</a></li>
<li class="section-crypto"><a href="#crypto-23">Does everyone need to be on your system (and using Mailpile) to be truly secure?</a></li>
<li class="section-crypto"><a href="#crypto-24">You don't mention anything about secure public key distribution. Is this a problem you plan to tackle?</a></li>
<li class="section-crypto"><a href="#crypto-25">If I write an email from my Mailpile to a friend's gmail, how does the encryption prevent his inbox from scanning the contents of my email?</a></li>
<li class="section-crypto"><a href="#crypto-26">Will you be storing my private key on your mail server?</a></li>
<li class="section-crypto"><a href="#crypto-27">Will Mailpile function similar to Lavabit and use different passwords for IMAP connections that are not related with private key password used to to decrypt mails?</a></li>
<li class="section-crypto"><a href="#crypto-28">Do you have plans to implement RFC6698 DANE, and move towards CA free authentication?</a></li>
<li class="section-crypto"><a href="#crypto-29">Do the mails stay encrypted in your servers or are they stored in plain text?</a></li>
<li class="section-crypto"><a href="#crypto-30">If e-mails are encrypted, how do you intend to implement a searching function?</a></li>
<li class="section-crypto"><a href="#crypto-31">So what exactly will be encrypted and what about the metadata?</a></li>
<li class="section-crypto"><a href="#crypto-32">Is Mailpile going to send PGP encrypted e-mail, where the mail body is encrypted, but all the headers and the metadata are not?</a></li>
<li class="section-crypto"><a href="#crypto-33">Or are you planning to somehow also encrypt the metadata (like in Bitmessage)? Would that even be possible with e-mail?</a></li>
<li class="section-crypto"><a href="#crypto-34">Will you use the Perfect Forward Secrecy in your mail ?</a></li>
<li class="section-crypto"><a href="#crypto-35">Will you implement start TLS in your e-mail system?</a></li>
<li class="section-crypto"><a href="#crypto-36">Will you hide the IP when send an e-mail with your service?</a></li>
<li class="section-crypto"><a href="#crypto-37">Does Mailpile automatically search for recipients keys or generate new keys which is then submited to the public key servers?</a></li>
<li class="section-crypto"><a href="#crypto-38">Does Mailpile support sending SMIME e-mails?</a></li>
<li class="section-crypto"><a href="#crypto-39">I send a lot of email, when it arrives on there servers is it decrypted or does decryption take place on the computer of the person who is supposed to receive it?</a></li>
</ul></li>
<li><a href="#tech">Technical Questions</a><ul>
<li class="section-tech"><a href="#tech-1">Will Mailpile run on Windows 8.1, Mac OSX, Linux etc. etc.?</a></li>
<li class="section-tech"><a href="#tech-2">Will mail sent from Mailpile be compatible with other e-mail clients?</a></li>
<li class="section-tech"><a href="#tech-3">Does Mailpile offer e-mail server hosting?</a></li>
<li class="section-tech"><a href="#tech-4">Will there be support for importing from Thunderbird, Outlook, Mac Mail, Eudora, etc...?</a></li>
<li class="section-tech"><a href="#tech-5">Can I migrate my mail from one server to Mailpile?</a></li>
<li class="section-tech"><a href="#tech-6">When signing up to websites using this email service, would my email address show up within the company I signed up to?</a></li>
<li class="section-tech"><a href="#tech-7">I  don't want my email to be full of illegal content (child porn) or viruses, how will you make that is possible? (Does the system scan for malware and remove them or at least warn us of suspect attachments).</a></li>
<li class="section-tech"><a href="#tech-8">Can you disable SPAM when using this server?</a></li>
<li class="section-tech"><a href="#tech-9">Can I install Mailpile on my dedicated server at OVH with Cent OS?</a></li>
<li class="section-tech"><a href="#tech-10">Will it run on Raspberry Pi? There are RPi collocation services that are promising.</a></li>
<li class="section-tech"><a href="#tech-11">Could you maybe leave in the possibility in Mailpile to manually download the font and plug it into the installation?</a></li>
<li class="section-tech"><a href="#tech-12">Will Mailpile  work on PowerPC / ARM architecture (I'm thinking of my Bubba 2 or future Bubba 3) since Mailpile is webmail. Would there be any issues for that with the necessary encryption libs / modules?</a></li>
<li class="section-tech"><a href="#tech-13">Will Mailpile change the Mail DNS server settings?</a></li>
<li class="section-tech"><a href="#tech-14">So with Mailpile will I be able to overcome my ISP mail limitations?</a></li>
<li class="section-tech"><a href="#tech-15">What about Linux? Are you coding Mailpile for Linux as well?</a></li>
<li class="section-tech"><a href="#tech-16">I have a super specific request how I'd like my email to be. Can you implement it?!</a></li>
<li class="section-tech"><a href="#tech-17">My friend just  said he'll use it if you have push support (probably  through an  exchange emulation, like how google apps has it).</a></li>
<li class="section-tech"><a href="#tech-18">Will you support multiple email accounts, not multiple user accounts (different people), this is multiple email accounts for one person.</a></li>
<li class="section-tech"><a href="#tech-19">Will messages be sent via SMTP from my regular address?</a></li>
<li class="section-tech"><a href="#tech-20">I have the server up and running exchange is set to journal mail to a specific account.  Where in mailpile do I specify that account to poll  emails?</a></li>
<li class="section-tech"><a href="#tech-21">I have a dedicated server with openbsd and postfix, I have apache, php, mysql. I can use Mailpile to give my users access webmail?</a></li>
</ul></li>
<li><a href="#dev">Contributing, Helping, Developing</a><ul>
<li class="section-dev"><a href="#dev-1">I am a developer, how can I help?</a></li>
<li class="section-dev"><a href="#dev-2">I am not a techie, how can I help?</a></li>
<li class="section-dev"><a href="#dev-3">Hi guys, I think your project is awesome, can we work together on something? I would like to work with/for you guys for my super cool project!</a></li>
<li class="section-dev"><a href="#dev-4">Can I be an official backer, with the stated reward, if I pay with Bitcoin?</a></li>
<li class="section-dev"><a href="#dev-5">Will you send me your IBAN and BIC code and name and address, so I can send you a financial support by bank?</a></li>
<li class="section-dev"><a href="#dev-6">I want to be a beta tester.</a></li>
</ul></li>
<li><a href="#wishlist">Feature Requests</a><ul>
<li class="section-wishlist"><a href="#wishlist-1">Are you going to include incoming filtering of messages to specific folders?</a></li>
<li class="section-wishlist"><a href="#wishlist-2">Is there the an ability to synchronize contact information with an external contact manager like Google contacts?</a></li>
<li class="section-wishlist"><a href="#wishlist-3">Will there be POP and IMAP support?</a></li>
<li class="section-wishlist"><a href="#wishlist-4">Will there be an app for Android?</a></li>
<li class="section-wishlist"><a href="#wishlist-5">Will there be an app for iPhone / iPad?</a></li>
<li class="section-wishlist"><a href="#wishlist-6">I'd like to write a Mailpile app... Can I do that?</a></li>
<li class="section-wishlist"><a href="#wishlist-7">I want an inbox that allows messages in and out from many different sources - email, SMS, voicemail, facebook, twitter, etc.</a></li>
<li class="section-wishlist"><a href="#wishlist-8">For the Linux / Unix geeks, like me, will there be command line utilities or interface?</a></li>
<li class="section-wishlist"><a href="#wishlist-9">Can I interact with Mailpile via XML-RPC?</a></li>
<li class="section-wishlist"><a href="#wishlist-10">Do you provide support for SMTP?</a></li>
<li class="section-wishlist"><a href="#wishlist-11">Make sure users can set different SMTP ports for outgoing mail as most ISPs block port 25</a></li>
<li class="section-wishlist"><a href="#wishlist-12">Make users should be allowed to choose rather or not SSL is enabled. SSL should be either a self signed key which Mailpile makes, or a key the user provides.</a></li>
<li class="section-wishlist"><a href="#wishlist-13">Make it easy to provide a configuration file with the SSL certificate for iOS</a></li>
<li class="section-wishlist"><a href="#wishlist-14">Can I choose to have Mailpile delete the email from the original server after download or keep it.</a></li>
<li class="section-wishlist"><a href="#wishlist-15">Have the option to auto port forward using NAT-PMP/UPnP and possibly offer a free DNS record on mailpile.is that is used as a dynamic DNS so users can access their mail by going to mrgecko.mailpile.is as an example.</a></li>
<li class="section-wishlist"><a href="#wishlist-16">Will Mailpile do automatic mail wiping?</a></li>
<li class="section-wishlist"><a href="#wishlist-17">Any plans to provide secure email accounts similar to what Lavabit did?</a></li>
<li class="section-wishlist"><a href="#wishlist-18">Can you backup the mails? / Since I understand they are stored in the computer the backup would be very important. Could the backup be automatic?</a></li>
<li class="section-wishlist"><a href="#wishlist-19">Will it be possible to send an encrypted email to several recipients at once?</a></li>
</ul></li>
<li><a href="#misc">Miscellanious Questions</a><ul>
<li class="section-misc"><a href="#misc-1">Which device would you recommend for us to use to enable maximum privacy?</a></li>
<li class="section-misc"><a href="#misc-2">Do you think that I could resell your service in Russia?</a></li>
<li class="section-misc"><a href="#misc-3">Where is your blog's RSS button!?!?!?!</a></li>
<li class="section-misc"><a href="#misc-4">Will the Alpha build in Jan 2014 be an open Alpha? Will we be allowed to install, use, and give feed back around that time?</a></li>
</ul></li></ul></div>
<ul class="list"><li class="faq-section-title" id="about"><h2>What is Mailpile?</h2></li>
<li class="faq-item" id="about-1"> <h3 class="faq-title">What is Mailpile?</h3> <span class="faq-section">about</span>
<p>Mailpile is email software (an app) that runs on your desktop or laptop computer. You interact with the program using your web browser. The goal of Mailpile is to allow people to send e-mail in a more secure and private manner than before.</p>
</li>
<li class="faq-item" id="about-2"> <h3 class="faq-title">Where does Mailpile store my mail?</h3> <span class="faq-section">about</span>
<p>With Mailpile, your e-mail is downloaded from the Internet (via an email server POP3 / IMAP), and stored locally on the computer where Mailpile is running.</p>
</li>
<li class="faq-item" id="about-3"> <h3 class="faq-title">Then how do I access it when my computer is turned off?</h3> <span class="faq-section">about</span>
<p>You don't! :-) for this reason, you may prefer to leave Mailpile running on a computer that is always on. You can then access it over the network using your web browser.</p>
</li>
<li class="faq-item" id="about-4"> <h3 class="faq-title">Is Mailpile webmail like Gmail, Yahoo, Hotmail?</h3> <span class="faq-section">about</span>
<p>Like common webmail, you use your web browser to access your Mailpile. However unlike most webmail solutions, Mailpile runs on "your own computer", so you have control over your data and your privacy. However, you can run Mailpile on a computer in the cloud (aka server). Confusion often comes from the fact that Gmail, Yahoo, and Hotmail are both email clients <a href="https://en.wikipedia.org/wiki/Email_client">(MUAs)</a> and email servers <a href="https://en.wikipedia.org/wiki/Message_transfer_agent">(MTAs)</a>. Thus, Mailpile is 50% "like" said services, and you can still use Mailpile (as a client) with Gmail as a server.</p>
</li>
<li class="faq-item" id="about-5"> <h3 class="faq-title">If I use Gmail, Yahoo, Hotmail with my Mailpile isn't my mail still going through their servers and kept there indefinitely?</h3> <span class="faq-section">about</span>
<p>Yes, your data would still be copied to Gmail, Yahoo, or Hotmail's servers (as well a a copy on your computer). If you started sending encrypted email, it would be leaving large encrypted blobs on their servers though :) </p>
</li>
<li class="faq-item" id="about-6"> <h3 class="faq-title">How much does Mailpile cost?</h3> <span class="faq-section">about</span>
<p>Mailpile is free of charge, you just download it and use it. It is also free of advertisements. Development is supported by voluntary donations from our community, from people like yourself who want a more secure and privacy friendly solution for e-mail. We accept donations here: <a href="https://www.mailpile.is/donate/">https://www.mailpile.is/donate/</a></p>
</li>
<li class="faq-item" id="about-7"> <h3 class="faq-title">I am a techie, can I change how Mailpile works?</h3> <span class="faq-section">about</span>
<p>Yes, Mailpile is 100% free, Open Source Software. You can find the source code online and make any changes you please here: <a href="https://github.com/pagekite/Mailpile">https://github.com/pagekite/Mailpile</a></p>
</li>
<li class="faq-item" id="about-8"> <h3 class="faq-title">If anyone can view the code &amp; change Mailpile, doesn't that make it less secure?</h3> <span class="faq-section">about</span>
<p>Quite the opposite, we believe Open Source facilitates peer review and quality engineering. If the entire community of security professionals can examine how Mailpile works under the hood, they can and will help us find and fix problems quicker than would otherwise be possible.</p>
</li>
<li class="faq-section-title" id="basic"><h2>Basic Questions?</h2></li>
<li class="faq-item" id="basic-1"> <h3 class="faq-title">What is Mailpile? Is it an email service?</h3> <span class="faq-section">basic</span>
<p>Mailpile is an email client used for encrypting/decrypting emails and not an email service. Mailpile does currently not issue its own email accounts/addresses. You can use your existing email address on top of Mailpile. If your existing email service stores your emails on  their servers, then they will not be able to read the encrypted emails. The Mailpile client is used for sending/receiving, managing, organizing and storing emails on your computer/USB/cloud. </p>
</li>
<li class="faq-item" id="basic-2"> <h3 class="faq-title">Is Mailpile real?</h3> <span class="faq-section">basic</span>
<p>Yes, and so are we!</p>
</li>
<li class="faq-item" id="basic-3"> <h3 class="faq-title">Is Mailpile ready yet?</h3> <span class="faq-section">basic</span>
<p>We launched an Alpha version for developers and advanced techies on Feb 1st 2014. A more user friendly Beta should be ready by late spring. Our 1.0 release will be in late summer 2014. For further details, check out our <a href="https://mailpile.is/blog/">blog</a>.</p>
</li>
<li class="faq-item" id="basic-4"> <h3 class="faq-title">Can we use Mailpile as the standard mail solution for our clients/company/server?</h3> <span class="faq-section">basic</span>
<p>When Mailpile is ready, that should be an option, yes.</p>
</li>
<li class="faq-item" id="basic-5"> <h3 class="faq-title">How can I get a MailPile account?</h3> <span class="faq-section">basic</span>
<p>There is no such thing! Mailpile is software you run on you computer, not an e-mail service provider. So you can just use the e-mail addresses you have already, or sign up for a new one somewhere.</p>
</li>
<li class="faq-item" id="basic-6"> <h3 class="faq-title">Can I get a cool @mailpile.is email address?</h3> <span class="faq-section">basic</span>
<p>No, unfortunately those are currently only for our core team members &amp; company. This may change in the future, or it may not. Absolutely no promises on this!</p>
</li>
<li class="faq-item" id="basic-7"> <h3 class="faq-title">Can I still Donate?</h3> <span class="faq-section">basic</span>
<p>Yes, we would love for you to <a href="https://mailpile.is/donate/">support us</a>.</p>
</li>
<li class="faq-item" id="basic-8"> <h3 class="faq-title">Is Mailpile always going to be free?</h3> <span class="faq-section">basic</span>
<p>Yes, it is a free and open software. However, to live in the current global economy, one has to have money to exchange for food. If you like it, <a href="https://mailpile.is/donate/">please consider donating</a>.</p>
</li>
<li class="faq-item" id="basic-9"> <h3 class="faq-title">Is there a mailing list so I can follow on your work?</h3> <span class="faq-section">basic</span>
<p>Not yet, but this is a good idea! We will think about it.</p>
</li>
<li class="faq-item" id="basic-10"> <h3 class="faq-title">How do I get updates about your project?</h3> <span class="faq-section">basic</span>
<p>We have an IRC channel on Freenode, #mailpile. This is the easiest to get hold of us and ask questions. Otherwise you can follow us on Twitter. Maybe in the future we'll consider having a mailing list. </p>
</li>
<li class="faq-item" id="basic-11"> <h3 class="faq-title">Regarding accessibility, what happens when my computer is offline?</h3> <span class="faq-section">basic</span>
<p>When the computer (laptop, desktop, webserver) you run your Mailpile from is offline, your Mailpile instance is no longer usable.</p>
</li>
<li class="faq-section-title" id="look"><h2>Branding and Design</h2></li>
<li class="faq-item" id="look-1"> <h3 class="faq-title">Does Mailpile allow me to customize my install with a company logo, colors, font?</h3> <span class="faq-section">look</span>
<p>Yes. We have been developing Mailpile to support this sort of functionality.</p>
</li>
<li class="faq-item" id="look-2"> <h3 class="faq-title">You used bad words in your video and I didn't like it.</h3> <span class="faq-section">look</span>
<p>We apologize you took offence to some of our branding and creative choices, we were just trying to have fun.</p>
</li>
<li class="faq-item" id="look-3"> <h3 class="faq-title">I don't like your design, logo, font, layout, haircut.</h3> <span class="faq-section">look</span>
<p>That is very sad, taste is subjective :(</p>
</li>
<li class="faq-item" id="look-4"> <h3 class="faq-title">I really liked your design, logo, font, layout, haircut.</h3> <span class="faq-section">look</span>
<p>Cheers, so do we :)</p>
</li>
<li class="faq-item" id="look-5"> <h3 class="faq-title">Why didn't you use a more modern color palate?</h3> <span class="faq-section">look</span>
<p>We thought more natural tones would humanize the user experience and make complicated things like encryption and email more user friendly.</p>
</li>
<li class="faq-item" id="look-6"> <h3 class="faq-title">Your font looks a bit fuzzy in my browser</h3> <span class="faq-section">look</span>
<p>Our font is currently still being developed. Currently, the "bold" weight is being generated in the browser, this is not a good way to do things (and looks really terrible in FireFox). Once we finish creating an actually bold weight webfont this will improve dramatically. The "mailpile" font will be released under a fully open &amp; free license- the SIL Open Font License (OFL)</p>
</li>
<li class="faq-section-title" id="usability"><h2>Interface and Usability Design</h2></li>
<li class="faq-item" id="usability-1"> <h3 class="faq-title">Will there be Open Source Smileys/Emoticons available in Mailpile?</h3> <span class="faq-section">usability</span>
<p>We haven't discussed that, so no. However, it is an open source project so if you want to make emoticons then you can.</p>
</li>
<li class="faq-item" id="usability-2"> <h3 class="faq-title">Do you have any plans to implement threaded conversations, like gmail?</h3> <span class="faq-section">usability</span>
<p>Yes, this is currently implemented. However, our design is slightly more "conversation" style that single line snippets.</p>
</li>
<li class="faq-item" id="usability-3"> <h3 class="faq-title">How do we make it easy enough for our elders to use?</h3> <span class="faq-section">usability</span>
<p>We will do our best to grandma proof everything in Mailpile.</p>
</li>
<li class="faq-item" id="usability-4"> <h3 class="faq-title">Will there be any similarities to Eudora?</h3> <span class="faq-section">usability</span>
<p>None of our team are Eudora users, but we strive to provide all the features popular email clients have.</p>
</li>
<li class="faq-item" id="usability-5"> <h3 class="faq-title">I don't find many programs that exist well in both the Windows and the Mac worlds. How do you plan to deliver this experience?</h3> <span class="faq-section">usability</span>
<p>Mailpile runs inside a web browser using HTML, CSS, and Javascript which 99% of the time is identical on both Mac and Windows. </p>
</li>
<li class="faq-item" id="usability-6"> <h3 class="faq-title">PGP encryption should be made simple. Does Mailpile's interface do this?</h3> <span class="faq-section">usability</span>
<p>Yes! That is our goal :)</p>
</li>
<li class="faq-item" id="usability-7"> <h3 class="faq-title">Will Mailpile inform users if an email they received was encrypted or not?</h3> <span class="faq-section">usability</span>
<p>Yes, Mailpile currently does this, as well as emails that are partially encrypted.</p>
</li>
<li class="faq-item" id="usability-8"> <h3 class="faq-title">Will the composing interface make it easy to choose whether I want to encrypt or not encrypt an email?</h3> <span class="faq-section">usability</span>
<p>Yes, we have a put a lot of time into thinking about and designing this to be intuitive.</p>
</li>
<li class="faq-item" id="usability-9"> <h3 class="faq-title">Is installing Mailpile going to be a simple double-click icon that once installed just opens a browser and loads Mailpile?</h3> <span class="faq-section">usability</span>
<p>Yes, that is the goal. Perhaps even a headless instance of a web kit that runs separately on your normal browser.</p>
</li>
<li class="faq-item" id="usability-10"> <h3 class="faq-title">Why isn't there more access to PGP encryption via the web interface?</h3> <span class="faq-section">usability</span>
<p>This is an alpha release. We are definitely going to expose more of our PGP encryption interface to the web user interface like adding, signing and deleting of keys as well as other things. Development is in progress.</p>
</li>
<li class="faq-item" id="usability-11"> <h3 class="faq-title">I do not want automatically grouped conversations. I cannot track this way. Does your program do that too?</h3> <span class="faq-section">usability</span>
<p>The conversations are threaded, but we are considering if we will change that in the future.</p>
</li>
<li class="faq-item" id="usability-12"> <h3 class="faq-title">I love your mail client do you know its cpanel ready?</h3> <span class="faq-section">usability</span>
<p>We are currently quite far from having a cpanel, but we plan to have it in the future. At the moment we are working hard on our Beta which is planned for this summer.</p>
</li>
<li class="faq-section-title" id="crypto"><h2>Encryption and Security</h2></li>
<li class="faq-item" id="crypto-1"> <h3 class="faq-title">Is Mailpile an encrypted email service?</h3> <span class="faq-section">crypto</span>
<p>Mailpile is not an email service, it is an email client. But Mailpile does support strong encryption.</p>
</li>
<li class="faq-item" id="crypto-2"> <h3 class="faq-title">What is your PGP public key?</h3> <span class="faq-section">crypto</span>
<p>Our team PGP key is downloadble from here: https://www.mailpile.is/files/team@mailpile.is.asc</p>
</li>
<li class="faq-item" id="crypto-3"> <h3 class="faq-title">Can you please include <em>insert-some-random-encrypted-service</em>.</h3> <span class="faq-section">crypto</span>
<p>Yeah, we'll get right to that - after we get the widely adopted protocols supported robustly ;)</p>
</li>
<li class="faq-item" id="crypto-4"> <h3 class="faq-title">I was looking for a private email server that can hide my email address from everyone that I haven't mailed to, does your service provide this?</h3> <span class="faq-section">crypto</span>
<p>Nope. That's actually impossible. If anybody tells you they can do this, they are probably lying. Sorry!</p>
</li>
<li class="faq-item" id="crypto-5"> <h3 class="faq-title">Is  it possible to delete a message that you send to someone, but you don't want them to keep in their account after certain period? (If not it should be developed).</h3> <span class="faq-section">crypto</span>
<p>No, that isn't possible. You can't un-tell somebody something. You can ask them nicely to delete the mail, but if they decide not to, you can't make them. Sorry. Nobody is going to be able to develop that feature in a way that is guaranteed to work, ever. This isn't a James Bond movie.</p>
</li>
<li class="faq-item" id="crypto-6"> <h3 class="faq-title">Can you create a pseudonym email address that only the recipient can see to identify us and send us message to, but it does not reveal my actual email address?</h3> <span class="faq-section">crypto</span>
<p>That's not really a part of the intended use of Mailpile. Somebody might provide this kind of service though - it sounds useful!</p>
</li>
<li class="faq-item" id="crypto-7"> <h3 class="faq-title">How will you prevent governments from accessing your user database?</h3> <span class="faq-section">crypto</span>
<p>Simple: We will not have a user database. We do not have any server infrastructure that contains user information. Users install the Mailpile client on their own computers. We do not track people that want to use Mailpile.</p>
</li>
<li class="faq-item" id="crypto-8"> <h3 class="faq-title">How safe is it to store email metadata in RAM (Random-access memory)?</h3> <span class="faq-section">crypto</span>
<p>It's pretty safe. If your computer is compromised, the storage is probably compromised anyway and you will have bigger things to worry about than your email account.</p>
</li>
<li class="faq-item" id="crypto-9"> <h3 class="faq-title">Will it, by default, deploy using encrypted configuration data?</h3> <span class="faq-section">crypto</span>
<p>Yes. Currently this is a configuration option which is turned off by default, but before our first stable release we will switch to having configuration data encrypted by default.</p>
</li>
<li class="faq-item" id="crypto-10"> <h3 class="faq-title">Would it possible to add support for one-time passwords?</h3> <span class="faq-section">crypto</span>
<p>This sounds reasonable. There are a lot of two-factor authentication methods we may consider implementing.</p>
</li>
<li class="faq-item" id="crypto-11"> <h3 class="faq-title">How secure is the database? Is it stored on an encrypted volume?</h3> <span class="faq-section">crypto</span>
<p>Yes. All configuration data, including the search index, will be encrypted by default when we get to the full release.</p>
</li>
<li class="faq-item" id="crypto-12"> <h3 class="faq-title">How are attachments stored? Are they encrypted, as well?</h3> <span class="faq-section">crypto</span>
<p>They are stored wherever your email is stored. If that's secure, the attachments are secure. We will provide methods to secure your email, although we recommend you should be using a full disk encryption!</p>
</li>
<li class="faq-item" id="crypto-13"> <h3 class="faq-title">Will search work with encrypted files? Or, are they residing on some encrypted file system, and seem un-encrypted to it?</h3> <span class="faq-section">crypto</span>
<p>Mailpile decrypts incoming emails, indexes them, and re-encrypts them. The search index is stored encrypted, and the terms are stored as hashes. Good enough?</p>
</li>
<li class="faq-item" id="crypto-14"> <h3 class="faq-title">Does Mailpile have no weak points when it comes to privacy/security? How can they be closed?</h3> <span class="faq-section">crypto</span>
<p>Yes. Email metadata is hard to secure, because the standards don't really allow for keeping it all secret. We can't do much about that. Also, if the recipient of your email doesn't have a publicly available encryption key, you can't send them encrypted email. Sorry, that's the way public key cryptography works.</p>
</li>
<li class="faq-item" id="crypto-15"> <h3 class="faq-title">The decrypted message is vulnerable/visible on compromised system? Can it be obfuscated?</h3> <span class="faq-section">crypto</span>
<p>If your system is compromised, you have a very big problem that Mailpile can't really help you solve. We will try to do what we can, but endpoint security is very important.</p>
</li>
<li class="faq-item" id="crypto-16"> <h3 class="faq-title">Will Mailpile work with .onion (Tor) domains?</h3> <span class="faq-section">crypto</span>
<p>We plan to provide support for that.</p>
</li>
<li class="faq-item" id="crypto-17"> <h3 class="faq-title">Will it work when residing on an in-Tor server?</h3> <span class="faq-section">crypto</span>
<p>Yes!</p>
</li>
<li class="faq-item" id="crypto-18"> <h3 class="faq-title">Will Mailpile support address aliases for incoming mail? (132txche6763fhjf@domain.onion = green_leaf_dude@domain.onion)</h3> <span class="faq-section">crypto</span>
<p>That's really up to the mail server to decide. Mailpile is a mail client, not a mail server. Sorry!</p>
</li>
<li class="faq-item" id="crypto-19"> <h3 class="faq-title">Isn't email forwarding a possible breach of security?</h3> <span class="faq-section">crypto</span>
<p>Yes, it is. It's also unavoidable. We can't prevent people from forwarding information - even if we were to do all sorts of magic to make it impossible in Mailpile, somebody could still write down your email on a postcard and send it to a friend. This is called the analog gap. The only solution is, don't send secrets in email to people you don't trust.</p>
</li>
<li class="faq-item" id="crypto-20"> <h3 class="faq-title">How will this service compare with something like Hushmail which claims to offer message en/decryption in browser as well as IMAP (if one pays).</h3> <span class="faq-section">crypto</span>
<p>Hushmail stores your email data on their servers. Mailpile does not have servers and we do not store users email. One can use Mailpile for free to send &amp; receiving encrypted email through any IMAP servers.</p>
</li>
<li class="faq-item" id="crypto-21"> <h3 class="faq-title">Is MailPile a viable non-centralized solution to issues like those faced by other privacy focused email companies like Lavabit or Silent Circle?</h3> <span class="faq-section">crypto</span>
<p>Yes, this is one of our core beliefs and underlying design principles.</p>
</li>
<li class="faq-item" id="crypto-22"> <h3 class="faq-title">What happens when you are communicating with people who are still hosted by Google or a self hosted insecure server? Do they need to implement something too?</h3> <span class="faq-section">crypto</span>
<p>People can continue using gmail or their acamdemic institutions email "server" as Mailpile is just the "client" that allows for sending of encrypted messages.</p>
</li>
<li class="faq-item" id="crypto-23"> <h3 class="faq-title">Does everyone need to be on your system (and using Mailpile) to be truly secure?</h3> <span class="faq-section">crypto</span>
<p>In order to send encrypted email all recipients need to have public &amp; private PGP keys and be encrypting their messages. Many other email clients allow people to send PGP encrypted emails. Hopefully, Mailpile is the easiest to use ;)</p>
</li>
<li class="faq-item" id="crypto-24"> <h3 class="faq-title">You don't mention anything about secure public key distribution. Is this a problem you plan to tackle?</h3> <span class="faq-section">crypto</span>
<p>We plan to attach users public keys with outgoing emails. Additionally, since some instances of Mailpile will be accessible over the web, that makes for interesting new opportunities for sharing of keys.</p>
</li>
<li class="faq-item" id="crypto-25"> <h3 class="faq-title">If I write an email from my Mailpile to a friend's gmail, how does the encryption prevent his inbox from scanning the contents of my email?</h3> <span class="faq-section">crypto</span>
<p>As long as both people use encryption, even if one or both people have @gmail.com addresses, Gmail cannot read encrypted email data even if the data ends up being stored on Gmail's servers.</p>
</li>
<li class="faq-item" id="crypto-26"> <h3 class="faq-title">Will you be storing my private key on your mail server?</h3> <span class="faq-section">crypto</span>
<p>No. We do not have servers and we do not store users private keys. You install our software on your computer which keeps your key nice, safe, and under your control.</p>
</li>
<li class="faq-item" id="crypto-27"> <h3 class="faq-title">Will Mailpile function similar to Lavabit and use different passwords for IMAP connections that are not related with private key password used to to decrypt mails?</h3> <span class="faq-section">crypto</span>
<p>No. Mailpile is entirely different than Lavabit.</p>
</li>
<li class="faq-item" id="crypto-28"> <h3 class="faq-title">Do you have plans to implement RFC6698 DANE, and move towards CA free authentication?</h3> <span class="faq-section">crypto</span>
<p>We are uncertain about this at the moment.</p>
</li>
<li class="faq-item" id="crypto-29"> <h3 class="faq-title">Do the mails stay encrypted in your servers or are they stored in plain text?</h3> <span class="faq-section">crypto</span>
<p>We don't have servers, so no. We do not store your emails. Messages are stored on your computer and encrypted with Open PGP. This does not include headers and metadata. However, Mailpile will encrypt metadata on your disc using AES-256-CBC at the moment, with a plan to move to AES-256-GCM in the future for tagging purposes. The keys for the AES are stored in the configuration file, which is PGP encrypted. </p>
</li>
<li class="faq-item" id="crypto-30"> <h3 class="faq-title">If e-mails are encrypted, how do you intend to implement a searching function?</h3> <span class="faq-section">crypto</span>
<p>Mailpile decrypts incoming e-mails, index them, and re-encrypts them. The search index is stored and also encrypted as well as the terms which are stored as hashes. Good enough?</p>
</li>
<li class="faq-item" id="crypto-31"> <h3 class="faq-title">So what exactly will be encrypted and what about the metadata?</h3> <span class="faq-section">crypto</span>
<p>The e-mail body will be encrypted. We are trying to find ways to make most of the metadata encrypted as well, but some of it can't be because of how e-mail works.</p>
</li>
<li class="faq-item" id="crypto-32"> <h3 class="faq-title">Is Mailpile going to send PGP encrypted e-mail, where the mail body is encrypted, but all the headers and the metadata are not?</h3> <span class="faq-section">crypto</span>
<p>Yes. We are experimenting with ways to encrypt headers as well using standard PGP + SMTP protocols.</p>
</li>
<li class="faq-item" id="crypto-33"> <h3 class="faq-title">Or are you planning to somehow also encrypt the metadata (like in Bitmessage)? Would that even be possible with e-mail?</h3> <span class="faq-section">crypto</span>
<p>We're going to try and encrypt all the metadata using PGP + SMTP, but e-mail still requires that some of the metadata be un-encrypted so that mail servers will know where to deliver it to. We plan on integrating Bitmessage before 1.0</p>
</li>
<li class="faq-item" id="crypto-34"> <h3 class="faq-title">Will you use the Perfect Forward Secrecy in your mail ?</h3> <span class="faq-section">crypto</span>
<p>We can't actually guarantee that without breaking a vital part of e-mail's functionality: people want to be able to read their old e-mails. If we implemented PFS, then nobody could ever view their archives. We consider this an antifeature, so we won't even try. Instead, we're going to just try to protect your e-mail as well as we can while it is in transit (using PGP and opportunistic SSL), and as well as we can when it is at rest (using PGP, mostly).</p>
</li>
<li class="faq-item" id="crypto-35"> <h3 class="faq-title">Will you implement start TLS in your e-mail system?</h3> <span class="faq-section">crypto</span>
<p>Of course. Although we do urge all e-mail providers to provide TLS natively, because, while opportunistic encryption is better than no encryption, it's way better to support always-on encryption.</p>
</li>
<li class="faq-item" id="crypto-36"> <h3 class="faq-title">Will you hide the IP when send an e-mail with your service?</h3> <span class="faq-section">crypto</span>
<p>We aren't providing a sending service. Our e-mail client can't obfuscate IP addresses - but if you route your mail through Tor or a Mixmaster, it might improve things for you.</p>
</li>
<li class="faq-item" id="crypto-37"> <h3 class="faq-title">Does Mailpile automatically search for recipients keys or generate new keys which is then submited to the public key servers?</h3> <span class="faq-section">crypto</span>
<p>Yes we search &amp; create keys. We are not sure yet about automatically submitting to keyservers.</p>
</li>
<li class="faq-item" id="crypto-38"> <h3 class="faq-title">Does Mailpile support sending SMIME e-mails?</h3> <span class="faq-section">crypto</span>
<p>No.  We are working on pgp/mime first, getting the metaphors and the UI right before we add alternate encryption schemes. S/MIME is also generally based on PKI which the general consumer may not have easy access to. We expect it'll be supported in the future.</p>
</li>
<li class="faq-item" id="crypto-39"> <h3 class="faq-title">I send a lot of email, when it arrives on there servers is it decrypted or does decryption take place on the computer of the person who is supposed to receive it?</h3> <span class="faq-section">crypto</span>
<p>You do not have any control over how the recipients of your mail is going to PGP decrypt the encrypted emails they receive from you, since the setup of emails can vary a lot.</p>
</li>
<li class="faq-section-title" id="tech"><h2>Technical Questions</h2></li>
<li class="faq-item" id="tech-1"> <h3 class="faq-title">Will Mailpile run on Windows 8.1, Mac OSX, Linux etc. etc.?</h3> <span class="faq-section">tech</span>
<p>Yes.</p>
</li>
<li class="faq-item" id="tech-2"> <h3 class="faq-title">Will mail sent from Mailpile be compatible with other e-mail clients?</h3> <span class="faq-section">tech</span>
<p>Yes! We are compliant with all the appropriate internet and e-mail standards.</p>
</li>
<li class="faq-item" id="tech-3"> <h3 class="faq-title">Does Mailpile offer e-mail server hosting?</h3> <span class="faq-section">tech</span>
<p>We don't offer that at the moment. We might in the future. Others currently do.</p>
</li>
<li class="faq-item" id="tech-4"> <h3 class="faq-title">Will there be support for importing from Thunderbird, Outlook, Mac Mail, Eudora, etc...?</h3> <span class="faq-section">tech</span>
<p>We already support importing data from various common formats. We're going to try and support all the popular formats over time.</p>
</li>
<li class="faq-item" id="tech-5"> <h3 class="faq-title">Can I migrate my mail from one server to Mailpile?</h3> <span class="faq-section">tech</span>
<p>Yes, but note that Mailpile is not a mail server - you're still going to have to have one of those somewhere - Mailpile is an email client.</p>
</li>
<li class="faq-item" id="tech-6"> <h3 class="faq-title">When signing up to websites using this email service, would my email address show up within the company I signed up to?</h3> <span class="faq-section">tech</span>
<p>That will depend on how the service you signup on has implemented Mailpile. Our software allows people to keep/use their existing addresses.</p>
</li>
<li class="faq-item" id="tech-7"> <h3 class="faq-title">I  don't want my email to be full of illegal content (child porn) or viruses, how will you make that is possible? (Does the system scan for malware and remove them or at least warn us of suspect attachments).</h3> <span class="faq-section">tech</span>
<p>You should probably run anti-virus software on your computer - Mailpile won't have that. We will provide a spam filter, which can be configured to keep out some nasty stuff. But realistically, all filters are flawed. In particular, it is very very hard to explain to a computer what is illegal - pretty much impossible. Humans are always going to have to exercise some level of good judgement.</p>
</li>
<li class="faq-item" id="tech-8"> <h3 class="faq-title">Can you disable SPAM when using this server?</h3> <span class="faq-section">tech</span>
<p>We will provide a spam filter. "Disabling spam" is a high bar - but we will do what we can as well as provide tools you can use to manually filter.</p>
</li>
<li class="faq-item" id="tech-9"> <h3 class="faq-title">Can I install Mailpile on my dedicated server at OVH with Cent OS?</h3> <span class="faq-section">tech</span>
<p>Sure! We like acronyms!</p>
</li>
<li class="faq-item" id="tech-10"> <h3 class="faq-title">Will it run on Raspberry Pi? There are RPi collocation services that are promising.</h3> <span class="faq-section">tech</span>
<p>Yes! Mailpile can run on Linux. Linux can run on Raspberry Pi. Therefore... we look forward to seeing people experiment with this, actually.</p>
</li>
<li class="faq-item" id="tech-11"> <h3 class="faq-title">Could you maybe leave in the possibility in Mailpile to manually download the font and plug it into the installation?</h3> <span class="faq-section">tech</span>
<p>We made our own font. It's bundled with Mailpile! Yay!</p>
</li>
<li class="faq-item" id="tech-12"> <h3 class="faq-title">Will Mailpile  work on PowerPC / ARM architecture (I'm thinking of my Bubba 2 or future Bubba 3) since Mailpile is webmail. Would there be any issues for that with the necessary encryption libs / modules?</h3> <span class="faq-section">tech</span>
<p>You won't have any problems. Mailpile is written in Python, so it's very portable.</p>
</li>
<li class="faq-item" id="tech-13"> <h3 class="faq-title">Will Mailpile change the Mail DNS server settings?</h3> <span class="faq-section">tech</span>
<p>No, Mailpile is a mail client - if you want to update your DNS, you'll have to do it through your registrar.</p>
</li>
<li class="faq-item" id="tech-14"> <h3 class="faq-title">So with Mailpile will I be able to overcome my ISP mail limitations?</h3> <span class="faq-section">tech</span>
<p>Mailpile is not an email server, so our software will not be able to help you achieve this goal.</p>
</li>
<li class="faq-item" id="tech-15"> <h3 class="faq-title">What about Linux? Are you coding Mailpile for Linux as well?</h3> <span class="faq-section">tech</span>
<p>Two of our three core developers do everything on Linux. We're not even entirely sure how to use all those other OS's... ;)</p>
</li>
<li class="faq-item" id="tech-16"> <h3 class="faq-title">I have a super specific request how I'd like my email to be. Can you implement it?!</h3> <span class="faq-section">tech</span>
<p>Not right now, maybe in the future. We are just three guys trying to get a beta ready in the summertime, but it's open source so you can play with it too!</p>
</li>
<li class="faq-item" id="tech-17"> <h3 class="faq-title">My friend just  said he'll use it if you have push support (probably  through an  exchange emulation, like how google apps has it).</h3> <span class="faq-section">tech</span>
<p>We like this idea, and we would like to implement it at some point, but it's not on our current roadmap.</p>
</li>
<li class="faq-item" id="tech-18"> <h3 class="faq-title">Will you support multiple email accounts, not multiple user accounts (different people), this is multiple email accounts for one person.</h3> <span class="faq-section">tech</span>
<p>Yes, this feature is in development.</p>
</li>
<li class="faq-item" id="tech-19"> <h3 class="faq-title">Will messages be sent via SMTP from my regular address?</h3> <span class="faq-section">tech</span>
<p>Yes, absolutely, Mailpile is an email client that inter-operates with the standard email protocol SMTP.</p>
</li>
<li class="faq-item" id="tech-20"> <h3 class="faq-title">I have the server up and running exchange is set to journal mail to a specific account.  Where in mailpile do I specify that account to poll  emails?</h3> <span class="faq-section">tech</span>
<p>We do not have any experience with setting Mailpile up with exchange servers. Please find our wiki on GitHub where you can try to find out how to get started with this.</p>
</li>
<li class="faq-item" id="tech-21"> <h3 class="faq-title">I have a dedicated server with openbsd and postfix, I have apache, php, mysql. I can use Mailpile to give my users access webmail?</h3> <span class="faq-section">tech</span>
<p>Once we have a stable release (our Beta release is planned for end of July this year) you should be  able to download the Mailpile client and store it on your server.</p>
</li>
<li class="faq-section-title" id="dev"><h2>Contributing, Helping, Developing</h2></li>
<li class="faq-item" id="dev-1"> <h3 class="faq-title">I am a developer, how can I help?</h3> <span class="faq-section">dev</span>
<p>You can take a look at our Github page and figure out if there's something to do there. </p>
</li>
<li class="faq-item" id="dev-2"> <h3 class="faq-title">I am not a techie, how can I help?</h3> <span class="faq-section">dev</span>
<p>You can spread the word about the awesomeness of Mailpile! </p>
</li>
<li class="faq-item" id="dev-3"> <h3 class="faq-title">Hi guys, I think your project is awesome, can we work together on something? I would like to work with/for you guys for my super cool project!</h3> <span class="faq-section">dev</span>
<p>We're happy that you have a super cool project and that you think our project is awesome. Right now, we are working very hard on getting Mailpile up and running and we are not looking for getting involved in extra projects as that would take time!</p>
</li>
<li class="faq-item" id="dev-4"> <h3 class="faq-title">Can I be an official backer, with the stated reward, if I pay with Bitcoin?</h3> <span class="faq-section">dev</span>
<p>You can be an official backer even if you don't pay with Bitcoin!</p>
</li>
<li class="faq-item" id="dev-5"> <h3 class="faq-title">Will you send me your IBAN and BIC code and name and address, so I can send you a financial support by bank?</h3> <span class="faq-section">dev</span>
<p>Yes. At some point.</p>
</li>
<li class="faq-item" id="dev-6"> <h3 class="faq-title">I want to be a beta tester.</h3> <span class="faq-section">dev</span>
<p>Excellent! Beta release is planned for the end of July 2014. Stay tuned!</p>
</li>
<li class="faq-section-title" id="wishlist"><h2>Feature Requests</h2></li>
<li class="faq-item" id="wishlist-1"> <h3 class="faq-title">Are you going to include incoming filtering of messages to specific folders?</h3> <span class="faq-section">wishlist</span>
<p>Yes, we use "Tags" instead of folders, but they function similarly. We also have a filters feature that works with Tags.</p>
</li>
<li class="faq-item" id="wishlist-2"> <h3 class="faq-title">Is there the an ability to synchronize contact information with an external contact manager like Google contacts?</h3> <span class="faq-section">wishlist</span>
<p>We will support importing of contacts from Google Contacts, but not synchronizing back to Google. However, someone may make a plugin to do so.</p>
</li>
<li class="faq-item" id="wishlist-3"> <h3 class="faq-title">Will there be POP and IMAP support?</h3> <span class="faq-section">wishlist</span>
<p>Yes. Soon.</p>
</li>
<li class="faq-item" id="wishlist-4"> <h3 class="faq-title">Will there be an app for Android?</h3> <span class="faq-section">wishlist</span>
<p>Not yet, no. But in the future yes.</p>
</li>
<li class="faq-item" id="wishlist-5"> <h3 class="faq-title">Will there be an app for iPhone / iPad?</h3> <span class="faq-section">wishlist</span>
<p>Perhaps, but we are not excited about Apple's App Store policies as well as their known involvement with the NSA.</p>
</li>
<li class="faq-item" id="wishlist-6"> <h3 class="faq-title">I'd like to write a Mailpile app... Can I do that?</h3> <span class="faq-section">wishlist</span>
<p>Sure you can. But realize that you're writing with pre-alpha code or alpha code.</p>
</li>
<li class="faq-item" id="wishlist-7"> <h3 class="faq-title">I want an inbox that allows messages in and out from many different sources - email, SMS, voicemail, facebook, twitter, etc.</h3> <span class="faq-section">wishlist</span>
<p>We think this is REALLY cool, hopefully our community will help us make awesome plugins that make this a reality faster!</p>
</li>
<li class="faq-item" id="wishlist-8"> <h3 class="faq-title">For the Linux / Unix geeks, like me, will there be command line utilities or interface?</h3> <span class="faq-section">wishlist</span>
<p>Yes, absolutely, this currently exists as much of our team of Linux / Unix geeks.</p>
</li>
<li class="faq-item" id="wishlist-9"> <h3 class="faq-title">Can I interact with Mailpile via XML-RPC?</h3> <span class="faq-section">wishlist</span>
<p>Maybe.</p>
</li>
<li class="faq-item" id="wishlist-10"> <h3 class="faq-title">Do you provide support for SMTP?</h3> <span class="faq-section">wishlist</span>
<p>Yes, this is currently implemented.</p>
</li>
<li class="faq-item" id="wishlist-11"> <h3 class="faq-title">Make sure users can set different SMTP ports for outgoing mail as most ISPs block port 25</h3> <span class="faq-section">wishlist</span>
<p>Users can specify this from the "Settings" interface.</p>
</li>
<li class="faq-item" id="wishlist-12"> <h3 class="faq-title">Make users should be allowed to choose rather or not SSL is enabled. SSL should be either a self signed key which Mailpile makes, or a key the user provides.</h3> <span class="faq-section">wishlist</span>
<p>This is a great idea. We will hopefully implement features for SSL like this once we get further a long :)</p>
</li>
<li class="faq-item" id="wishlist-13"> <h3 class="faq-title">Make it easy to provide a configuration file with the SSL certificate for iOS</h3> <span class="faq-section">wishlist</span>
<p>We are not sure how much we want to develop towards supporting Apple's heavily walled (and surveilled) garden, but consider accessing a mobile web app of Mailpile served from a Raspberry Pi on an iOS device</p>
</li>
<li class="faq-item" id="wishlist-14"> <h3 class="faq-title">Can I choose to have Mailpile delete the email from the original server after download or keep it.</h3> <span class="faq-section">wishlist</span>
<p>Yes, once POP &amp; IMAP is implemented we will support this feature.</p>
</li>
<li class="faq-item" id="wishlist-15"> <h3 class="faq-title">Have the option to auto port forward using NAT-PMP/UPnP and possibly offer a free DNS record on mailpile.is that is used as a dynamic DNS so users can access their mail by going to mrgecko.mailpile.is as an example.</h3> <span class="faq-section">wishlist</span>
<p>This is an interesting idea that we are considering.</p>
</li>
<li class="faq-item" id="wishlist-16"> <h3 class="faq-title">Will Mailpile do automatic mail wiping?</h3> <span class="faq-section">wishlist</span>
<p>Inbox zero is a noble goal. Is that what you meant? We hope to encourage &amp; work on plugins to achieve this goal.</p>
</li>
<li class="faq-item" id="wishlist-17"> <h3 class="faq-title">Any plans to provide secure email accounts similar to what Lavabit did?</h3> <span class="faq-section">wishlist</span>
<p>No plans to do what Lavabit did as they were a centralized solution. Decentralization is one of our main end goals. We are considering offering services (relays, servers) that make the sending of email more secure + allow for decentralization + are sustainable + user friendly.</p>
</li>
<li class="faq-item" id="wishlist-18"> <h3 class="faq-title">Can you backup the mails? / Since I understand they are stored in the computer the backup would be very important. Could the backup be automatic?</h3> <span class="faq-section">wishlist</span>
<p>The idea is to decentralize emails and not to collect them and store them.  This is why Mailpile is an email client and not an email server. The users are supposed to store their emails themselves in their computers or on USB sticks, so that they will have full ownership and power over their emails, meaning they are not stored with a 3rd party. Therefore, people will have to make and store the backups themselves. For automatic backups you could probably find a software that would do that for you on your computer.</p>
</li>
<li class="faq-item" id="wishlist-19"> <h3 class="faq-title">Will it be possible to send an encrypted email to several recipients at once?</h3> <span class="faq-section">wishlist</span>
<p>Yes it is possible to send an encrypted mail to several recipients at once. It is encrypted with multiple different keys. It should be possible in the Alpha version already, but if it turns out to be bugged, then wait for the Beta version that is planned for release at the end of July 2014.</p>
</li>
<li class="faq-section-title" id="misc"><h2>Miscellanious Questions</h2></li>
<li class="faq-item" id="misc-1"> <h3 class="faq-title">Which device would you recommend for us to use to enable maximum privacy?</h3> <span class="faq-section">misc</span>
<p>This question might take a while to answer. In the meantime, check out https://securityinabox.org/. It's a good start!</p>
</li>
<li class="faq-item" id="misc-2"> <h3 class="faq-title">Do you think that I could resell your service in Russia?</h3> <span class="faq-section">misc</span>
<p>Feel free!</p>
</li>
<li class="faq-item" id="misc-3"> <h3 class="faq-title">Where is your blog's RSS button!?!?!?!</h3> <span class="faq-section">misc</span>
<p>Good question. Here: http://www.mailpile.is/blog/index.rss</p>
</li>
<li class="faq-item" id="misc-4"> <h3 class="faq-title">Will the Alpha build in Jan 2014 be an open Alpha? Will we be allowed to install, use, and give feed back around that time?</h3> <span class="faq-section">misc</span>
<p>Absolutely. The Alpha release will require a bit of tech knowledge and use the command line to get up and running. The Beta (July 2014) will be much easier.</p>
</li></ul>
</div>
<!-- Features -->
<div id="features" class="add-top">
	
	<h3>Feature State</h3>
	<table border="0" cellpadding="0" cellspacing="0" class="full-width-table rounded add-bottom">
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-search"></span></td>
		<td>Search</td>
		<td class="features-table-desc">API based search interface allows complex emails queries</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-message"></span></td>
		<td>Inbox</td>
		<td class="features-table-desc">Avatar view or compact text based. Normal or threaded inbox</td>
		<td class="features-table-status">Stable</td>
	</tr>			
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-compose"></span></td>
		<td>Compose</td>
		<td class="features-table-desc">Simple and clean way to attach things and send encrypted emails</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-lock-closed"></span></td>
		<td>Encryption</td>
		<td class="features-table-desc">PGP encryption and verification of emails and recipients</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-signature-verified"></span></td>
		<td>Signatures</td>
		<td class="features-table-desc">Easily determine if inbound email is from who it says it is from</td>
		<td class="features-table-status">Stable</td>
	</tr>	
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-user"></span></td>
		<td>Contacts</td>
		<td class="features-table-desc">Secure address book supports VCard &amp; importing of current contacts</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-tag"></span></td>
		<td>Tags</td>
		<td class="features-table-desc">Assign single or multiple tags to emails</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-spam"></span></td>
		<td>Spam Detection</td>
		<td class="features-table-desc">Being handled quite well by spambayes</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-attachment"></span></td>
		<td>Attachments</td>
		<td class="features-table-desc">Easily attach pictures and files to your emails</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-groups"></span></td>
		<td>Groups</td>
		<td class="features-table-desc">An easy way to contact groups of people &amp; organize their responses</td>
		<td class="features-table-status">Started</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-photos"></span></td>
		<td>Photos</td>
		<td class="features-table-desc">Browse photo album like views of all your photo attachments</td>
		<td class="features-table-status">Started</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-document"></span></td>
		<td>Files</td>
		<td class="features-table-desc">Automatic organization of file attachments</td>
		<td class="features-table-status">Started</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-themes"></span></td>
		<td>Themes</td>
		<td class="features-table-desc">Switch between different themes that best suit your liking</td>
		<td class="features-table-status">Started</td>
	</tr>	
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-later"></span></td>
		<td>Send Later</td>
		<td class="features-table-desc">Delay when an email gets sent</td>
		<td class="features-table-status">Started</td>
	</tr>
	</table>

	<h3>Importing</h3>
	<table border="0" cellpadding="0" cellspacing="0" class="full-width-table rounded add-bottom">
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>Mbox</td>
		<td class="features-table-desc">Importing of archived emails</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>Maildir</td>
		<td class="features-table-desc">Importing of archived emails</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>Thunderbird</td>
		<td class="features-table-desc">Importing of Thunderbird emails & contacts</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>Gmail</td>
		<td class="features-table-desc">Importing of archived emails, labels, and access to new email</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>Apple Mail</td>
		<td class="features-table-desc">Importing of archived emails from Mac Mail</td>
		<td class="features-table-status">Development</td>
	</tr>
	</table>

	<h3>Protocols</h3>
	<table border="0" cellpadding="0" cellspacing="0" class="full-width-table rounded add-bottom">	
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-routes"></span></td>
		<td>SMTP</td>
		<td class="features-table-desc">Sending of email to remote services</td>
		<td class="features-table-status">Stable</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>IMAP</td>
		<td class="features-table-desc">Importing of archived emails, labels, and access to new email</td>
		<td class="features-table-status">Stable</td>
	</tr>			
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-inbox"></span></td>
		<td>POP3</td>
		<td class="features-table-desc">Connect and import archived emails, folders, and access to new email</td>
		<td class="features-table-status">Development</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-tor"></span></td>
		<td>Tor</td>
		<td class="features-table-desc">Send and receive e-mail or access your Mailpile over Tor</td>
		<td class="features-table-status">Development</td>
	</tr>
	<tr>
		<td align="center" valign="middle" class="features-table-icon"><span class="icon-routes"></span></td>
		<td>SMTorP</td>
		<td class="features-table-desc">Send and receive email peer-2-peer over Tor</td>
		<td class="features-table-status">Development</td>
	</tr>
  </table>

</div>