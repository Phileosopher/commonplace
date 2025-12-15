
## Protection

MAKE SURE TO CONSIDER [INSURANCE]

it's worth noting the security/efficiency tradeoff

- a cysec policy that's too constricting will prevent people from ever getting work done (e.g., can't even view a powerpoint file from a flash drive and can't send it via email)

[F*ck Cybersecurity : cybersecurity](https://old.reddit.com/r/cybersecurity/comments/12aumfx/fck_cybersecurity/)

- The comments indicate it well:
- Your mission isn't to safeguard assets. Your mission is to help bring cyber risk in line with company policy. If you advise X, Y and Z because A and they say no because B, you document it and go get a Coke.
- There's something very wrong about corporate awfulness, and that's cysec for you.

## Tentative Sections

- Honeypot
- Managed Security Services
- Forensics
- Recovery
- Destruction

## memory destruction

### Morgan Stanley Lost Some Hard Drives - Matt Levine

Don't throw out your computers
Well here's my new financial heist movie script. A big bank has a lot of computers that keep track of its customers' accounts. It periodically buys new computers to do a better job of keeping track of those accounts. When it does that, it hires a moving company to cart away all of the old computers. The moving company makes a few extra bucks by selling the old computer hardware to, I don't know, scrappy small technology businesses that are happy to have the bank's slightly outdated hardware. Ideally the bank, or the moving company, would delete all the data on the computers first, but that takes time and time is money and sometimes they forget.
So what you do is, you set up a scrappy small tech business as a cover, and you go to the bank's moving company's computer sale and buy all the computers, and then you turn them on and get all of the bank's customers' account information, and then you steal their money. Okay, having written this all out, I guess it is a boring heist movie, never mind. Still:

    The Securities and Exchange Commission today announced charges against Morgan Stanley Smith Barney LLC (MSSB) stemming from the firm's extensive failures, over a five-year period, to protect the personal identifying information, or PII, of approximately 15 million customers. MSSB has agreed to pay a $35 million penalty to settle the SEC charges.
    The SEC's order finds that, as far back as 2015, MSSB failed to properly dispose of devices containing its customers' PII. On multiple occasions, MSSB hired a moving and storage company with no experience or expertise in data destruction services to decommission thousands of hard drives and servers containing the PII of millions of its customers. Moreover, according to the SEC's order, over several years, MSSB failed to properly monitor the moving company's work. The staff's investigation found that the moving company sold to a third party thousands of MSSB devices including servers and hard drives, some of which contained customer PII, and which were eventually resold on an internet auction site without removal of such customer PII. While MSSB recovered some of the devices, which were shown to contain thousands of pieces of unencrypted customer data, the firm has not recovered the vast majority of the devices.

Great stuff. If you find a 2016-vintage Morgan Stanley computer on EBay and crack it open to find customer information, I guess you can … do … something with that? I don't know. Here, from the SEC complaint, is what one guy did:

    On October 25, 2017, nearly a year after the completion of the 2016 Data Center Decommissioning, MSSB received an email from an IT consultant in Oklahoma ("Consultant"). In that email, Consultant informed MSSB that he had purchased hard drives from an online auction site and that he had access to MSSB's data on those devices. In that email, Consultant informed MSSB that "[y]ou are a major financial institution and should be following some very stringent guidelines on how to deal with retiring hardware. Or at the very least getting some kind of verification of data destruction from the vendors you sell equipment to." MSSB eventually repurchased the hard drives in Consultant's possession.

Somehow the SEC neglects to mention how much Morgan Stanley paid him for those hard drives. How much would you charge Morgan Stanley for the hard drives in this situation? I do not want to give you legal advice, and I think that you would want to get some legal advice before trying this, but I think if you offered these hard drives to Morgan Stanley for, say, $100,000 each, they might pay you? Is there a bug bounty program for, you know, you threw out the wrong hard drive? They paid the SEC $35 million; there is money in the budget for this sort of thing.
The rest of the complaint is full of suggestive hints at the scale of Morgan Stanley's after-the-fact garbage hunt:

    In late 2017, MSSB launched an investigation into the disposition of the devices that were part of the 2016 Data Center Decommissioning project and determined that Moving Company had also delivered the 8,000 back-up tapes removed from one of the data centers to IT Corp B. MSSB emailed IT Corp B on January 19, 2018 asking whether IT Corp B could "confirm the disposition of …3k lbs of tapes." IT Corp B responded: "I can confirm that we did send this load of tapes for secure waste to energy incineration. Although that lot # is not the lot # we used. They were processed 'Confidential Material' in June of 2016." MSSB's basis for believing that these tapes were in fact destroyed without any unauthorized access to customer PII and consumer report information hinges on this email. MSSB has no other verification or 5 documentation that these tapes were destroyed.
    In June 2021, MSSB obtained another fourteen of the missing hard drives from a downstream purchaser. Based on forensic analysis of these hard drives, thirteen of the devices contained a total of at least 140,000 pieces of customer PII. The vast majority of the hard drives from the 2016 Data Center Decommissioning remain missing. …
    MSSB has identified an international shipping project that may have involved Moving Company. MSSB can state only that "documents suggest" that Moving Company transported 18-36 unspecified devices to a storage location in New York City. It was contemplated that those devices would be shipped internationally to Europe, potentially by Moving Company. 

Possibly thousands of ancient Morgan Stanley storage devices, all over the globe, possibly full of customer data, possibly useful for nefarious purposes. Probably not; there is no suggestion that anyone did anything at all nefarious with any of these things, and also not much suggestion that you could do anything particularly bad. (You're not supposed to hand out customers' "personal identifying information" to random hackers, but there's no suggestion that it was, like, account passwords.) 
More from
Bloomberg opinion
When Immigration Hypocrisy Landed on Martha's Vineyard
LinkedIn's Future Is a Joke
I Paid Off Student Loans But Support Relief for Those Who Can't
Don't Let the Crypto Winter Go to Waste
In recent years it has been popular for investment bank executives to say that they were becoming tech companies: They were hiring developers, building apps, talking about big data. This is a good thing to say, I suppose, insofar as being a tech company means that you can make large profits without putting too much of your own balance sheet at risk, that you can scale rapidly, that you can compete with Silicon Valley for employees.
But there is also an old-school understanding of investment banking in which it is a business of implicit knowledge, of personal connections, that the value that a good banker can add can't be reduced to an algorithm. There is a tension there. If banks are tech companies then they will invest in good consistent electronic communication tools that create good searchable records. If banking is a business of personal connections, then bankers will ignore those tools and text clients on their personal cell phones because that feels more personal. Morgan Stanley got fined $200 million for that this summer. You are supposed to use the official communication tools.
Similarly, if banking is a business of implicit knowledge, go ahead and throw out the old hard drives; what's important is the knowledge in the hearts and minds of the bankers. If banking is a data business, you should probably wipe the hard drives before you throw them out.
