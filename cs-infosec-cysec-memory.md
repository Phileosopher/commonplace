
# How to keep computer memory secure

The severity of hard drive security has created a popular convention that memory must be wiped multiple times for the information to be perfectly safe. Popular myths have been 7 passes, or even as many as 35 passes. While this may be true for magnetic drives (like the older platter hard disks or floppy disks), this isn't necessarily true for other drives (like optical disks or electrically-stored memory like USB/SSD).

The best memory security is to have an [encrypted](encryption.md) OS, then simply delete everything once (or more with magnetic storage), and make sure the information can't be migrated to another storage (i.e., limit access to files via USB peripherals, external media, and network).

If you're particularly concerned over a hard drive you're throwing out, permanently destroy it by running a power drill through the hardware.

Of course, this protects the drive from *other* people stealing it, but you still have to maintain data integrity and redundancy. This is where you'll need a [RAID configuration](cs-memory.md).

## Limiting computer access

Computer systems are presenting an inherent vector of attack when they're connected to the internet, so computers become safer when taken offline.

On the far end, data can be stored in a Sensitive Compartmentalized Information Facility (SCIF):

- This is typically a physical location (room, building, etc.) with specific physical security measures to keep classified information safe.
  - Those with access can view, store, print, or otherwise access the products.
  - Classified documents generally have to stay inside SCIFs, and documents can only come out if they're properly packaged to protect the information and carried by official couriers with special training, clearances, and lockable courier cases.
- SCIFs are rated for the classification level of information they contain, and all have strict access requirements including appropriate clearance, access lists and badges, no mobile devices, no earbuds, no smartwatches, etc.
  1. TS: Top Secret (exceptionally grave damage to National Security)
  2. S: Secret (grave damage to National Security)
  3. CUI: Controlled Unclassified Information (which replaced For Official Use Only - FOUO)
     - This includes things like personally identifiable info, or other things that we generally want to keep private but aren't strictly classified.
- Classification markings are not only on the cover sheet, but also throughout the document itself, which includes pages and individual paragraphs.
- One way of accidentally attaining a higher classification is to add multiple pieces of unclassified information together.
  - If someone isn't careful, the final document might be a higher classification due to the sum of its parts.
- There are also classified computer networks with no connection (air gaps) to the regular internet or outside world.
  - These are essentially self-contained and handle information up to a particular classification level.
  - These systems include email clients to allow sending documents to other users with access and the need to know.
- There are also unclassified computer systems for daily work that have internet connectivity, but are regulated by IT policies and systems that filter what someone can access.
  - If there's a bad link on the page (site, video, etc.), there's often an intimidatingly official-looking "ACCESS TO THIS SITE IS FORBIDDEN" in that space, or sometimes for the whole page.
- Also, even gaining access requires a symbolic colonoscopy of [compliance](cs-infosec-compliance.md) and background check requirements.

## Backups

The easiest way to protect computer information from being lost is to keep regular, consistent backups of everything. That way, if anything fails, you can revert to a "known good" configuration or set of files. The best way is through the 3-2-1 Backup Rule:

- 3 copies of the data
- 2 different types of storage
- 1 copy offsite (under your bed or office)

A backup can be cold or hot storage:

- A synchronized "hot storage" backup a long distance away, just in case your house is hit by a flood or tornado.
- A sporadically synchronized "cold storage", to hold known-good information indefinitely without a synchronization overwriting it.

A hard drive will eventually fail, and more quickly if it's consumer-grade. For a lasting backup, pay very close attention to "write tolerance" and "over-provisioning" to see how long that drive will last.

To prevent a lightning strike or power outage from destroying hardware, get an "uninterruptible power supply" (UPS). A power strip can stop surges, but a UPS will also give enough time to save any important work before powering off the computer.
