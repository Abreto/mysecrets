# mysecrets (v0.2)

## Requirement

* bash shell
* Git
* A [keybase](https://keybase.io) account and
[the Keybase app](https://keybase.io/download) (just command line).

## Structure

I will introduce you to each file. Don't close the window please, in spite of my
**poor** English.

###	.gitignore

As is universally acknowledged, `git` will ignore files listed in this file. And
I have added a line `*.raw` to it. So it is recommended that you should name all
your origin files as `*.raw`, making it easy to leave them local directory
and prevent them from uploaded to your remote repository (Probably means your
secrets are exposed to everyone). Of course, it's all up to you.

### keybase_recipient

The username you used in [keybase.io](https://keybase.io) (Like
[abreto](https://keybase.io/abreto) :)). It helps if no `\n` lies in the end of
this file.

### decrypt decrypt2file encrypt put get

Commands that I will give more details later.

## Usage

### Synchronize with your repository

Run

	$ ./get

to pull changes from your remote repository.

Run

	$ ./put

to push local changes to your remote repository. You can edit the variable
`repo`(repository) or `bran`(branch) in file `put`.

### Encrypt and Decrypt

#### Normal

Run

	$ ./encrypt <file1>[ <file2>[ <file3>[ ...]]]

to encrypt files following the command. Encrypted text will be stored in
`<filename>.asc`, and binary output will be stored in `<filename>.bin`.

-----

Run

	$ ./decrypt <file1>[ <file2>[ <file3>[ ...]]]

to decrypt files following the command. Decrypted message will be output to
`stdout`. As for `decrypt2file`, you can guess what he does!

-----

Visit [this page](https://keybase.io/decrypt), copy the content in `sth.asc` to
the textarea, enter your passphrase and just click `Decrypt`.

#### Advanced

Just an example. If all your origin files are saved as `*.raw`, you can run

	$ ./encrypt `ls *.raw`

to encrypt all your files in one line. But you are supposed to **innovate**(aka
imagine)!
