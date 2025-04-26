---
layout: default
---

# Change Owner Password

This command changes the password which is also known as the *set permissions password* or the *master password*. Have a look at some [examples](#examples).
 
## Usage

```
pdfcpu changeopw [-upw userpw] inFile opwOld opwNew
```

<br>

### [Common Flags](../getting_started/common_flags)

<br>

### Arguments

| name         | description            | required
|:-------------|:-----------------------|:--------
| inFile       | PDF input file         | yes
| opwOld       | current owner password | yes
| opwNew       | new owner password     | yes, must not be empty!

<br>

## Examples

You have to set the *owner password* when you `encrypt` a file and you can change it anytime later with `changeopw`.

Change the *owner password*:
```sh
$ pdfcpu encrypt -opw opw enc.pdf
writing enc.pdf ...

$ pdfcpu changeopw enc.pdf opw opwNew
writing enc.pdf ...
```
