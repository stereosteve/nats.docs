# Stream, Consumer, and Account Names

Stream, Consumer (durable name), and Account names are used in both the
subject namespace used by JetStream and the filesystem backing JetStream
persistence.  This means that when naming streams, consumers, and
accounts, names must adhere to subject naming rules as well as being
friendly to the file system.

We recommend the following guideline for stream, consumer, and account names:

* Alphanumeric values are recommended.
<<<<<<< HEAD
* Spaces, tabs, period \(`.`\), greater than \(`>`\) or asterix \(`*`\) are prohibited.
* Limit name length.  The JetStream storage directories will include the account,
stream name, and consumer name, so a generally safe approach would be to keep names
under 32 characters.
=======
* Spaces, tabs, period \(`.`\), greater than \(`>`\) or asterisk \(`*`\) are prohibited.
* Limit names to 255 characters or less.
>>>>>>> 60f3fbb79fa5c1aa9c6d18b3d45321820e228b77
* Do not use reserved file names like NUL, LPT1, etc.
* Be aware that some file systems are case insensitive so do not
  use stream or account names that would collide in a file system.
  For example, `Foo` and `foo` would collide on a Windows or Mac OSx System.

 We plan to address these limitations in a future release.