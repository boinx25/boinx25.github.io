---
layout: post
title: "Chrome Extension"
date: 2014-09-12 10:30:18 +0800
comments: true
categories: 
---

<p>Last monday, Sir Efren asked us to try and create a simple Google Chrome extension. I was assigned to do the Stock Quote Extension. I will show you how I built my own Extension.</p>
<br />

<h2>This is the project directory of my extension:</h2>
{% img /images/Directory.png 300 300 'image' 'images' %}
<br />
<h2>First:Created my manifest.json file.</h2>
{% img /images/manifest.png 800 500 'image' 'images' %}
<p>Your manifest file contains the details about your extension.</p>
<ul>
<li><p>Manifest Version - declares what version your manifest should be. It's currently should be set to 2 because 1 is already deprecated and the support for it is already phased out.</p></li>
<li><p>Name - this will be the name of your extension. This is what will the users see when they download or use when they search your extension.</p></li>
<li><p>Description - description for your extension. This is to explain to the users what your extension do.</p></li>
<li><p>Permissions - usually used to connect APIs to your extension. It is to permit the connection of your extension to the external API.</p></li>
<li><p>Browser Action - this is where you put what behavior will your extension do when clicked.</p></li>
		<ul>
			<li><p>Default icon - this will be the icon of your extension.</p></li>
			<li><p>Default popup - once the icon of your extension was clicked this will show up.</p></li>
		</ul>
<li><p>Content Scripts - this is where you declare external scripts, external css, etc.</p></li>
		<ul>
			<li><p>Matches - this specifies the pages where your script will be injected.</p></li>
			<li><p>scripts - this is where you specify the external script files that will be used. So that the extensions will run your script once it was clicked. Inline scripts are not accepted by the extension. You still have to include your scripts in the head tag of your html file.</p>
		</ul>
</ul>

<br />

<h2>Second:Created my html file</h2>
{% img /images/popup.png 800 500 'image' 'images' %}

<h2>Third:Created my js file</h2>
{% img /images/popupjs.png 800 500 'image' 'images' %}
<p>I created my own js file so that I can gather data from Yahoo's Stocks API then it will be printed to the table on the extension's popup.</p>

<br />

<h2>My extension when installed</h2>
{% img /images/ExtensionToolbar.png 300 300 'image' 'images' %}
<p>My extension is the one next to the PS Logo.</p>

<br />

<h2>My extension when clicked</h2>
{% img /images/ExtensionWorking.png 500 500 'image' 'images' %}
<p>Everytime the user clicks my extension it will return updated results from Yahoo's Stocks API.</p>
