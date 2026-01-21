---
title: "DNS Record Types Explained"
seoTitle: "DNS Record Types Explained"
datePublished: Wed Jan 21 2026 04:56:51 GMT+0000 (Coordinated Universal Time)
cuid: cmknjwkh7000a02jsadxjf7ty
slug: dns-record-types-explained
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1768970750175/bef74fba-5e77-4248-a5c4-d3d2d85a2190.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1768971269084/403f9ebe-4e47-4e8b-9377-133a03d08d8f.png
tags: chaicode

---

**How does a browser know where a website lives?**

You type:

```bash
https://example.com
```

And somehow your browser finds the correct server on the internet.

No guessing.  
No searching.  
No magic.

This works because of **DNS records**.

Let’s understand them slowly and simply.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768971125350/230496f3-43f6-4249-8c2e-57e6c995bd4c.png align="center")

## What Is DNS? (Very Simple Explanation)

DNS stands for **Domain Name System**.

DNS exists because:

* Humans like names ([`google.com`](http://google.com))
    
* Computers like numbers (`142.250.190.14`)
    

So DNS acts like a **phonebook of the internet**.

It answers one basic question:

> “For this name, where should I go?”

That answer is stored in DNS records.

## Why DNS Records Are Needed?

A domain name alone is just a label.

DNS records tell the internet:

* Which server hosts the website
    
* Who manages the domain
    
* Where emails should be delivered
    
* How other services should find it
    

Think of DNS records as **instructions**, not just data.

## NS Record — Who Is Responsible for This Domain?

**Problem it solves:**  
👉 “Who should I ask about this domain?”

An **NS (Name Server) record** says:

> “These servers are responsible for this domain.”

### Real-Life Example

Think of an apartment building.

* NS record = **building management office**
    
* They don’t know every detail
    
* But they know who does
    

Without NS records, DNS would not know **where to ask next**.

## A Record — Domain → IPv4 Address

**Problem it solves:**  
👉 “What is the IP address of this domain?”

An **A record** maps:

```bash
example.com → 93.184.216.34
```

This is the most common DNS record.

### Real-Life Example

* Website name = person’s name
    
* IP address = house address
    

When a browser wants to visit a site, it usually ends here.

## AAAA Record — Domain → IPv6 Address

**Problem it solves:**  
👉 Same as A record, but for IPv6

An **AAAA record** maps:

```bash
example.com → 2606:2800:220:1:248:1893:25c8:1946
```

Why does this exist?

* IPv4 addresses are running out
    
* IPv6 provides a much larger address space
    

### Simple Rule

* **A** = IPv4
    
* **AAAA** = IPv6
    

That’s it. Nothing more to memorize.

## CNAME Record — One Name Points to Another Name

**Problem it solves:**  
👉 “I don’t want to repeat IP addresses everywhere.”

A **CNAME (Canonical Name) record** says:

> “This name is an alias of another name.”

Example:

```bash
www.example.com → example.com
```

The browser then resolves [`example.com`](http://example.com) normally.

### Real-Life Example

* Nickname → real name
    
* “Call me John” → “My full name is Jonathan”
    

### Common Confusion: A vs CNAME

* **A record** → points to an IP
    
* **CNAME** → points to another domain name
    

You don’t use both for the same name.

## MX Record — How Emails Find Your Mail Server?

**Problem it solves:**  
👉 “Where should emails be delivered?”

An **MX (Mail Exchange) record** tells mail servers:

> “Send emails for this domain here.”

Example:

```bash
example.com → mail.example.com
```

### Important Detail

MX records don’t point directly to IPs.  
They point to **hostnames**, which then resolve using A or AAAA records.

### Real-Life Example

* Website address ≠ office mailroom
    
* MX record = mailroom location
    

## TXT Record — Extra Information & Verification

**Problem it solves:**  
👉 “How do I store extra instructions?”

A **TXT record** stores plain text.

Used for:

* Domain ownership verification
    
* Email security (SPF, DKIM, DMARC)
    
* Third-party integrations
    

### Real-Life Example

TXT records are like:

> Notes pinned on your door for visitors

They don’t route traffic, but they provide **proof and instructions**.

## How All DNS Records Work Together (One Website)?

Let’s take a single domain:

```bash
example.com
```

Here’s what happens:

* **NS records** → say who manages DNS
    
* **A / AAAA records** → tell browsers where the site lives
    
* **CNAME records** → provide aliases like `www`
    
* **MX records** → route emails correctly
    
* **TXT records** → verify and secure services
    

All of them solve **different problems** for the same domain.

## Clearing Common Beginner Confusion

### NS vs MX

* **NS** → DNS responsibility
    
* **MX** → email delivery
    

Different purposes. Different layers.

### A vs CNAME

* **A** → name → IP
    
* **CNAME** → name → name
    

One is direct. One is indirect.

## The Mental Model to Remember

DNS is not complicated.

It’s just answering questions like:

* Who manages this domain? → **NS**
    
* Where is the website? → **A / AAAA**
    
* Is this name an alias? → **CNAME**
    
* Where should email go? → **MX**
    
* Any extra instructions? → **TXT**
    

That’s it.

## Final Thoughts

DNS records are not “advanced networking”.

They’re just **labels and directions** that help the internet find things.

Once you understand:

* What problem each record solves
    
* How they work together
    

DNS stops feeling scary and starts feeling logical.