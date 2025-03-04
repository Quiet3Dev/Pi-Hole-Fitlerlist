# Pi-Hole Filterlist Blocklist
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This project started in January 2020, focusing on the differences between using "adlist/domains" and "denylist regex" when using low-end hardware like the Rasberry Pi Zero W or obsolete hardware based on 32-bit systems. The project ended around June 2022 since it worked with 32-bit systems and the Rasberry Pi Zero W was not overloaded with access times and updates.

Finally, "denylist regex" has become more efficient due to the elimination of the need to access the web to update blocklists, the use of local storage to hold regex lists, and the reduction of the number of CPU cycles required to update Pi-Hole and gain internet access. The reason "Adlist/Domains" failed in the end is because it updated the blocklist, taking a chance on whether a URL is alive or dead. If a dead URL cannot be updated until it is replaced, they could have removed all blocked domains if a live URL was available.

The folder inside "Adlist" contains the list as a text file if you want to download or modify the blocklist. The folder's categories are:

- Ads
- Crypto
- DNS, ISP, and VPN Blocking
- Drugs
- Fraud
- Gambling
- Other
- Malware
- Phishing
- Piracy
- NSFW
- Proxy
- Ransomware
- Redirect
- Scam
- Social
- Spam
- Torrent
- Tracking


# Everything  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The "Everything" blocklist contains almost all of the categories listed above, but it is constructed from a different blocklist that includes some of the categories removed from the previous blocklist. However, you might need to make your own allowlist in order to access some websites since the "Everything" category mostly blocks everything above.

- Everything


# Youtube 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Youtube's ad servers are constantly being updated, which invalidates blocklists. To bypass the ads on YouTube, you will need to install adblock. For Android, you will have to use a modified YouTube app to bypass ads or the Blockada app to block ads.

- Youtube

# Mixed Categories 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- 

There are mixed categories inside that can't be separated from the list because they have more than one category. For example:

- Ads, and Tracking 
- Ads, Crypto, and Malware
- Ads, and Malware

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The folder inside "Denylist Regex" contains a list as a text file. There are issues with regex lists since some code does not work properly with Pi-Hole. The folder's categories are:

- Ads and Tracking
- Ads Only
- Crypto
- DNS and VPN Blocking
- Everything
- Fraud
- Gambling
- Malware
- Phishing
- NSFW
- Social Media
- Tracking
- Youtube

# Youtube  
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The same problem exists with YouTube's "Adlist" blocklist: it can block some ads, but YouTube has multiple ad servers that could break the video stream.

- Youtube

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

If you want to check if your code is working properly, use "regex101.com" to see if there are any errors. Below is some information on how to create regex code and a website to make it easier to read regex code.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Videos to Help Create a Regex Denylist: 

https://www.youtube.com/watch?v=bgBWp9EIlMM

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Helpful Websites to Create Regex Code:

https://regex101.com/

https://www.debuggex.com/

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Updates       
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 -----------------------------
| Adlist - Updates Stopped |
 -----------------------------

The Pi-Hole "Adlist" is no longer updated because it consumes storage, time, testing, and cleanup. At the same time, find a similar blocklist and replace the old one; replacing the old blocklist could cause more problems. It is recommended to use a regex denylist because it does not rely on updating blocklists and instead relies on a small algorithm to block IP addresses from accessing websites or block websites that have suspicious links or functions.

 --------------------------------
| Regex Denylist - Slow Updates |
 --------------------------------

Fiterlist.com's regex denylist is being gradually updated. The lists used are from Adguard, AdBlock, Adblock Plus, and uBlock Origin. Some of the regex lists have some errors, and it will take a while to clean up some of the codes for Pi-Hole to accept some codes.

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

 -------------
|   Credits   |
 -------------

Majority Adlist and Regex Fitlerlist were found at "filterlists.com" by Collin M. Barrett.

The credits are in each file in the bottom section, since they will create a mess on the front page.
