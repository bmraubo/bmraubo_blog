---
title: How to DNS with gusto and confidence
date: 2021-09-24 10:48:47
tags:
---

IP addresses are unwieldy and hard (for humans) to remember. To make it easier, we use domain names - www.website.com. The Domain Name System translates the domain name into the IP address, facilitating the connection. The process of conversion between domain name and IP address is known as DNS resolution.

### DNS Process

There are four servers involved in the DNS resolution process.

1. <u>**The DNS recursor**</u> - Receives queries from client machines, and then makes queries of its own in order to provide a response. While technically it may have to make more than one query in order to reach the authoritative nameserver, caching is used to keep data from previous requests available (the cache being stored on the local machine for privacy reasons). 

2. <u>**Root nameserver**</u> - First step of the resolution process proper, it takes the query from the DNS recursor and returns the Top Level Domain (TLD) server. In our case, the Root nameserver would point the request to the '.site' TLD.

3. <u>**Top Level Domain server**</u> - This hosts the records related to the last portion of the hostname, in this case '.site'. The TLD server returns the IP address of the authoritative nameserver below. 

4. <u>**Authoritative Nameserver**</u> - This translates the specific query (eg. 'bmraubo') into an IP address for the connection.

5. <u>**Additional, Optional nameservers**</u> - where a subdomain exists, (e.g. blog.bmraubo.site *this is not a bad idea actually*) then the CNAME record for the subdomain is stored on a further authoritative nameserver, accessed through the higher level one.

Once all this is complete, the browser will have the IP address of the site being accessed, and makes an HTTP request to that address. So quite a lot of work goes on behind the scenes every time you access the webpage.

### DNS Caching

This is where DNS caching comes in - it enables the storage of IP addresses and their associated hostnames, expediting the resolution process. But there are risks involved.

Firstly, if the IP address of the website you are trying to access changes, then the cached information will point the browser in the wrong direction, resulting in a HTTP 404 error, even if the website is actually online. So regular cleaning of the DNS cache is required in order to maintain the accuracy of the directory as a whole.

Secondly, there is a security risk - the less regular the cleaning cycle, the more time there is for the IP address to be used for malicious purposes - for example, replacing a legitimate website with a phishing website. This is known as DNS poisoning or DNS spoofing 

Finally, from a privacy perspective, the cache holds a record of web browsing activity. Most operating systems and browsers create a DNS cache that is independent of browsing history and needs to be cleared separately. 

That's about it on the topic. I have tried to move this blog onto a subdomain, to allow me to use the general bmraubo.site domain name for other purposes down the line. This can take up to 24 hours to update... which means if I did something wrong it will be a while before I realise that.

