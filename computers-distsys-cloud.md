
# Cloud computing

You can use a computer locally on-premises("on-prem") or, with the power of the [internet](computers-networks.md), you can use it remotely.

If you use it remotely, your information is remotely accessible, or in the "cloud".

Cloud services can be public, private, or a hybrid. Public cloud shares the service across multiple users for a variety of reasons, while private is often for [security](computers-infosec.md) reasons to protect the information.

As far as cloud services, [Big Tech](computers-bigtech.md) maintains control over that market.

Amazon

- This was born from Amazon's internal attempt to recover from their [technical debt](habits-tech.md) starting in 2000.
- It was publicly launched in 2004 for the public as Amazon Web Services(AWS), an [IaaS](computers-distsys-enterprise.md).
- Amazon has a strange history of competing against itself, and AWS is considered a customer of Amazon even though the money all goes back to Amazon.
- Amazon has many, *many* services available with tons of customization.
  - However, there's a little bit of a learning curve to use it.
- Unfortunately, Amazon is also often a direct competitor to just about every industry at this point.

Microsoft

- This was from Microsoft's attempt to create reusable components for internal staff.
- It was announced in 2008 as Project Red Dog and released as Windows Azure in 2010 as IaaS, though it sucked and couldn't even run Windows Server at first, so they relaunched a much better product in 2013 and renamed it to Microsoft Azure in 2014.
- Azure is part of the Microsoft Intelligent Cloud business segment that also includes [GitHub](computers-software-versionctrl.md) and the server, cloud, support, and consulting parts of the Microsoft.
- However, Microsoft doesn't seem to report Azure independently for whatever reason.
- Since Microsoft has been B2B for ~40 years, they know what businesses want and how to give it to them.
- Microsoft, however, makes most of their money on software licenses, so [open-source](legal-ip-floss.md) is a direct competitor to their offerings, even if they work well with it because they have to.

Google

- They released Google App Engine in April 2008, but aimed for a PaaS approach unlike Microsoft and Amazon.
- Over a few years, they grew like crazy, and have expanded their product range.
- Google Cloud Platform and Google Workplace (formerly G Suite) are part of the Google company.
- Unfortunately, since Google's profit model is more on user data, it's reasonable to assume they'll scrape *everything* you store in their cloud and use it.
  - Google also has a history of deprecating their services, meaning they're not reliable in the long-term.

It's not really reliable to indicate the key customers of any cloud service provider because a vast corporation may have one tiny subdivision that pays and barely uses a cloud provider.

Altogether, the lesser of the evils between Google, Microsoft, and Amazon for any private citizen is likely Microsoft.

- Amazon is a direct competitor to just about any business most people could do.
- Google is unreliable, and they will sunset programs without sufficient warning.
- Microsoft, however, hasn't gone anywhere and tends to move slowly.

There are other Big Tech cloud providers as well that are worth examining for most situations:

- IBM (established in 1911)
- Oracle's Cloud (established in 1977)
- SAP (established in 1972 in Germany)
- Alibaba (established in 1999, though it's owned by China)

## Storage

The simplest and most common method of cloud storage involves simply synchronizing [files](computers-files.md). This can be one-way or both ways, and can be periodic or constant. Most cloud services (e.g., Dropbox, OneDrive) are both ways and constant, since it's *darn* convenient across multiple computers.

For redundant storage with important computer files, it's a generally good idea to have "network-attached storage" (NAS), which typically keeps a backup of whatever is stored locally. It also can help to have "snapshots" of various points in the past, just in case there was a detected deletion that synchronized back to the NAS.

Further, cloud storage can be as-needed, where all the files are displayed for access but require download to properly use. This compromise saves local storage space while allowing full access to whatever is needed, presuming an [internet connection](computers-networks.md). For space reasons, most mobile device storage apps use this, but most desktop computer apps don't use it as of 2021 except OneDrive.

## Virtualization

One of the most thorough and straightforward ways to remotely access apps and storage in a cloud environment is through a "virtual desktop environment" (VDI). To the user, it looks like a locally hosted [OS](computers-os.md), but is actually using a remote desktop [protocol](standards-computers.md) to access a [virtual machine](computers-distsys-vm.md).
