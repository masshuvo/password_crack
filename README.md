# password_crack
This is the full guide of cracking different type of file.


Crack password

# Pdf

<details> <summary>PDF</summary> PDF ↓

  How to create a PDF file in Linux↓

<b> Image to PDF without password.</b>  </br>

<code> convert image.jpg image.pdf </code> </br>


### For multiple: 
<code> convert image1.jpg image2.png image3.gif output.pdf </code>


</br> 


# Image to PDF with password: 

### Tool: sudo apt-get install imagemagick pdftk

### Convert the image to PDF using ImageMagick:
<code> convert input_image.jpg intermediate.pdf </code>
</br>

### Use pdftk to set a password for the PDF:
<code> pdftk intermediate.pdf output final_protected.pdf owner_pw 12345A#% user_pw 12345A#% </code> </br>

<b> Replace input_image.jpg with your image file and final_protected.pdf with your desired output PDF file name. </b>

</br>

This process creates a password-protected PDF with owner password (owner_pw) and user password (user_pw) set to "12345A#%". The owner password allows full control over the PDF, while the user password restricts certain operations like opening the PDF without providing the password.

### Remember to adjust the file paths and names as needed.

# single password and single user

first you need to convert your file to PDF </br>
<code> convert input_image.jpg intermediate.pdf </code> </br>
### Use qpdf to set a password for the PDF:
<code> qpdf --encrypt "your_password" "your_password" 40 -- intermediate.pdf final_protected.pdf </code> </br>

Example: <code> qpdf --encrypt "123" "123" 256 -- pic1.pdf pic2.pdf </code>

<p> Replace "your_password" with the desired password and adjust file paths as needed.</p>

# Password cracking method:
tool: pdfcrack 
Example: <code> pdfcrack -w file.pdf pass.txt </code>



-------------------------------------------------------
</details>

# Zip
<details> <summary>ZIP</summary>   


</Details>

# Tar
<details> <summary>TAR</summary>   

</Details>

# 7z
<details> <summary>7z</summary>   

</Details>

# RaR
<details> <summary>RAR</summary>   

</Details>
