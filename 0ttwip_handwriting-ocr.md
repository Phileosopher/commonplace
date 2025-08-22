
One of the earliest forms of computer programming came through marking information on a specialized tabulated piece of paper. It allowed entering information, and had the small advantage of being asynchronous input (i.e., prepare the papers, then feed them in later).

"Optical mark recognition" (OMR) is still useful for multiple-choice [tests in schools](pedagogy.md) (informally called "scantrons"), but scanning in fixed information only has limited use compared to the conveniences of [a keyboard](computers-keyboard.md).

## Scanning

A scanner ends up producing the same abstraction as a [camera](camera.md): a recorded image. However, the primary difference between the two is that a scanner will work line-by-line while a camera captures the image as instantaneously as possible.

The primary advantage of a scanner is that it can capture [text](computers-keyboard.md) better, since it's taking proportionally more time to acquire the information. However, scanners are also cheaper than cameras because of that same reality.

In one sense, a flatbed scanner works a bit like the reverse of a [printer](computers-printers.md): slowly move from one side to another, often with a light to illuminate the information, and a sensor captures the image and converts it into [encoded color](graphics.md) line-by-line.

Scanners come in various forms:

- Flatbed scanner - place a sheet on a piece of glass and cover it up, then the sensor/light assembly creeps along underneath it to get the image.
- Sheetfed scanner - aka "auto document feeder" (ADF) scanner, place a pile of sheets on a device that looks a bit like a personal printer, then run a batch of them.
- Photo scanner - a flatbed scanner, but much higher quality.
- Portable scanner - a smaller and lower-quality scanner that can sometimes fit in a pocket, useful for gathering lots of [information](database.md) for review later.
- Multifunction scanner/printer/copier - a multi-tool [marketed](marketing.md) as a [money-saving](money-4_spending.md) purchase that does nothing particularly well.

The primary [driver](computers-os.md) technology that runs scanners is called "TWAIN", which is a reference to "never the twain shall meet" in light of how difficult connecting a scanner to a computer can be. That's not an exaggeration, and printer/scanner technology is irritatingly difficult to [break-fix](fix.md) for approximately the same sorts of reasons.

## Reading text

To convert a photo to text, computers use software called "optical character recognition" (OCR), which employs the straightforward idea of parsing letters to make sense of them. It tends to only work with known fonts.

Detecting characters in text is an exercise in tedium and typographical analysis. Even though it's *usually* reliable, a semi-grainy scan of a PDF file can still yield inaccurate text. To that end, most OCR still needs a human to review the quality of the finished text recognition.

The OCR can be part of the scanner's firmware, or it could be software-based *after* it's been converted to a file.

Often, OCR images can have transcription errors over familiar text (e.g., "a" is misrepresented as "e"), and even slight rotations of an image can severely hamper its effectiveness.

"Intelligent character recognition" (ICR), or "intelligent OCR", is a more advanced form of OCR that parses text beyond standard OCR, typically by training through [machine learning](computers-ai-ml.md). When properly trained, it can typically track handwriting styles and a vast variety of fonts, and an even more advanced form of ICR can work with identifying entire words altogether (IWR).

If a computer can *read* text, it's a trivial additional step for it to be able to *create* it as well.

Broadly speaking, there are several major standards to scan documents:

1. Scan as an image, with no metadata or text recognition overlay.
2. Scan a TIFF file, which can keep images high-quality, but not all software supports them, and there aren't many advanced features to the file.
3. Scan a PDF file, which has *all* the possible features, and is versatile across most software, but has many complicated elements that can hamper its usefulness.

The PDF protocol was designed by Adobe to replace all the usefulness of paper, and contains a *vast* collection of features:

- Bookmarks for referencing locations.
- [Password-protection](computers-cysec-authentication.md) and [encryption](encryption.md) of the file itself.
- [Metadata](computers-files.md) storage, for just about anything.
- Multiple layers for annotations, OCR, form fills, signatures, write-protection, and read-protection.
- Hidden text (functionally similar to [HTML's](computers-webdev.md) [image](graphics.md) alt text).
- The ability to embed audio and video into the PDF file.
- The means to run an early version of JavaScript inside it.
- Compression to trim the memory from everything above.

All these extra features can create a nightmare for building a clean aesthetic in PDF files. Often, a copy-paste from PDF can pick up too many spaces, remove spaces altogether, incorrectly parse paragraphs or words, swap out text order, or simply treat text as a raw image. This is also assuming that the PDF isn't write-protected.

Unfortunately, [fixing](fix.md) PDF files only involves a few possible solutions:

1. Spool the PDF out through a software [printer](computers-printers.md) to another PDF with the "Save to PDF" feature. This removes or merges most of the layers.
2. Delete all the metadata and extra content that's not visible, then repeatedly run OCR on it.
3. Decompress and parse the encoded text, [which is a massive headache](https://gist.github.com/senderle/8ad6aae251c4ddf9424f8a05dd0e8c18).

## Reading codes

In the 1940s, the "barcode" was invented by Bernard Silver as a means for computers to quickly read information. The original premise of the barcode was essentially the dots and dashes of Morse code, but drawn vertically as lines.

While development of the technology was relatively slow compared to others, barcodes became a ubiquitous part of retail by the 1980s once stores standardized Universal Product Codes (UPCs) to [track inventory](accounting.md).

A counter-intuitive aspect of barcodes is that the data itself is contained in the *white* spaces, not the black ones. This was a design feature to make it easier to read in dim light, and most laser barcode readers can read barcodes even in near-darkness because of it.

The next evolution of barcodes came in 1994 with a "Quick Response" code (QR), invented by the Toyota subsidiary Denso Wave for labeling automobile parts.

- Most of the elements are stored twice to allow reading when partially obscured.
- A QR code is a square symbol with equally shaped squares on 3 of the sides called finder patterns, which tell the software which way is up. The fourth side on the bottom right also has an alignment pattern that helps determine the code's orientation and angle.
- There are also evenly spaced dots on the inside left and top of the square near the finder patterns called the timing pattern that determine how large the code is. Version 1 is the smallest, and it can go up to Version 40.
- Around the perimeter of the finder patterns, there is format information that indicates "error correcting code" (ECC) and a mask pattern that evens out black-and-white areas by inverting some of them (since QR codes work best with even amounts of black and white background).

Ironically, QR codes have *not* been quick-response. While they've been adopted by many retailers (e.g., restaurants), they're much slower than a standard barcode, especially with a cellphone [camera](camera.md).

While it's less popular, the Aztec code is another advanced barcode created in 1995. It has a center symbol with a bullseye pattern, which has the size of the grid encoded in it. This gives it the unique advantage that it does *not* need white space around it to correctly read it (since the size and center of the grid is already indicated).

## Barcode issues

*Every* conversion from analog information (i.e., OCR, barcode, scanner) to computer data has built-in risks of the data being corrupted.

Unfortunately, it's not uncommon for information to parse incorrectly, even with [plenty of testing](computers-software-redesign.md).

- [Xerox machines had a non-OCR bug which changed numbers on its scans that persisted for 8 years](https://www.dkriesel.com/en/blog/2013/0802_xerox-workcentres_are_switching_written_numbers_when_scanning).

From [a design standpoint](design-uxui.md), adding barcode technology to an inherently social experience (e.g., restaurants, concerts) can create a *very* antisocial experience altogether, especially if people are conditioned to social interaction in a [culture](culture.md).

* * * * *

## Additional reading

[GRAIL Text Recognizer](https://jackschaedler.github.io/handwriting-recognition/)

[QR codes](https://typefully.com/DanHollick/qr-codes-T7tLlNi)
