# 📮 Barcode Bonanza - L08 C04

Intel just in!

On doing a routine review of all the boxes of Cola on one of the ships, we found four boxes with additional barcode stickers on them. Nobody can account for how they got there or what they mean. It must be The Chiquitoos on the inside sending each other messages about which boxes to target.

See if you can read the barcodes, decode the output and put them in the right order to get the message.

**Tip:** The flag is in the decrypted message.

<details><summary>

## Need a hint?</summary>

> 💡 Hint: Try searching online for "bar code reader" or a similar term. The codes have been split up; you may have to try decoding them in all possible combinations to get the answer, which is encoded with a common encoding scheme.

</details>

## Files

- [barcode-01.5f1bbd80.jpg](/assets/barcodebonanza2.jpg)
- [barcode-02.260c39ba.jpg](/assets/barcodebonanza1.jpg)
- [barcode-03.8a0d5fc8.jpg](/assets/barcodebonanza3.jpg)
- [barcode-04.ef6ea7da.jpg](/assets/barcodebonanza4.jpg)

<details><summary>

## Step by Step</summary>

- Download each image and put it through an online Barcode reader or decoder
- The series of outputted strings should look like the following
  - xNOGZCTgo=
  - cnlOcGRNcm
  - ogME9JZUJt
  - RmxhZz
- Rearrange these segments into all different combinations and decode them with [Base64](https://www.base64decode.org/)
- The correct arrangement is as follows
- `RmxhZzogME9JZUJtcnlOcGRNcmxNOGZCTgo=`

</details>
