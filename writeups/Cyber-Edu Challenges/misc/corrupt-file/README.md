<h1>Corrupted-file</h1>

<img width="578" alt="Screenshot 2022-11-15 223027" src="https://user-images.githubusercontent.com/107073731/202022546-f8a3982b-bdb7-40c1-96ff-f901ff04c8cf.png">


We see that the the file we download has the .zip extension. Let's unzip it using: <i><p> unzip flag.docx.zip </i></p>

<p> When we open this file using nano or any other text editor this is what we'll see: </p>

<img width="848" alt="nano" src="https://user-images.githubusercontent.com/107073731/202023823-9eef66e9-af43-4885-8e54-488671392f75.png">


We might think this is a word file because of the .word extension but if we do: <i><p> file flag.docx </i></p>

We see it is a .xz file

<img width="458" alt="file" src="https://user-images.githubusercontent.com/107073731/202024437-41b4cb82-bf6d-4dca-8374-db01799df94e.png">

So what do we do ? Well, we rename the file to have .xz extension and decompress it.


<img width="497" alt="xz extension" src="https://user-images.githubusercontent.com/107073731/202025401-09c9e2c6-5821-49f7-bfcd-373087362acc.png">

Now if we do a simple cat command we will see the flag:

<img width="846" alt="flag" src="https://user-images.githubusercontent.com/107073731/202025523-b6b18786-c27c-47ef-8a11-58d2b3fe2529.png">
