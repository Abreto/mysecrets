# mysecrets

All your plain text or other origin files must be named as `*.raw` or `*/*.raw`.
Run

	./encrypt <file1>[ <file2>[ <file3>[ ...]]]
	./put

to encrypt (needs [keybase](https://keybase.io/download "Download keybase").
please edit the file `keybase_recipient` to your username in [keybase.io](https://keybase.io)
(without any `\n` at the end of file) first.) and push your encrypted files to
your repo.


---

Run

	./get
	./decrypt <file1>[ <file2>[ <file3>[ ...]]]

to view the data before encrypting.
