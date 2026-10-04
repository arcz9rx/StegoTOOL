A simple web-based steganography tool written in html that hides encrypted, compressed text inside an image and allows a user to unlock it later with a passphrase.

Features:
1.AES Encryption & Passphrase Protection: Encrypts secret messages before embedding them into images.
2.Data Compression: Maximizes available image capacity prior to encoding.
3.Customizable LSB Depth: Adjust the number of Least Significant Bits (1–8) per color channel to balance storage capacity against visual image quality.
4.Alpha Channel Support: Option to utilize the alpha (transparency) channel for increased data storage.
5.Capacity Check: Pre-calculates whether a message fits within a selected image before generating the output.
6.Lossless PNG Output: Guarantees pixel-exact preservation of embedded data upon download.

HOW TO USE:
a)Hiding a Message:
•Open StegoTool.html in any modern browser.
•Under Hide message, click Choose File and select a cover image.
•Enter your secret text in the Message field.
•Provide a secret Passphrase (required for decryption).
•Set your preferred LSB depth and choose whether to check Use alpha channel.
(Optional) Click Check capacity to verify your message fits inside the image.
•Click Create PNG to generate and download the output image containing your hidden payload.

b)Extracting a Message:
•Under Extract message, click Choose File and select the encoded PNG file.
•Enter the exact Passphrase used during encoding.
•Match the original LSB depth and Use alpha channel settings.
•Click Unlock message. The decrypted text will populate in the Recovered message box.

Technical Overview:
LSB steganography works by altering the least significant bits of an image's pixel color channels (Red, Green, Blue, and optionally Alpha). Because changing the lowest bits causes imperceptible color shifts to the human eye, the image appears visually unchanged while carrying binary data.

Note: Any lossy compression (such as converting the final image to JPEG or re-saving it through messaging apps that compress media) will corrupt the LSB data. Always store and transfer the resulting file as an uncompressed, lossless PNG.
