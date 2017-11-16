+++
title= "Making a GPG Key"
date= 2017-11-16T08:39:40+05:45
description = ""
draft= false
# Type of content, set "slide" to display it fullscreen with reveal.js
type="page"
# Creator's Display name
creatordisplayname = "Siddhant Rimal"
# Creator's Email
creatoremail = "siddhantrimal@hotmail.com"
# LastModifier's Display name
lastmodifierdisplayname = "Siddhant Rimal"
# LastModifier's Email
lastmodifieremail = "siddhantrimal@hotmail.com"
+++

1. Check for already existing GPG
	```
	gpg --list-secret-keys --keyid-format LONG

	```

2. Generate a key(_If not exist in #1 _)

	```
	gpg --gen-key
	```
	{{%alert info %}}
Default Selections are RSA 4096. Enter for unlimited validity or, be paranoid. Enter Real Name, Email, Comment to set the hash.
{{%/alert%}}


3. Check the list to see if key exists now
	```
	gpg --list-secret-keys --keyid-format LONG

	```

4. If exists, use the KeyID such as `3EC4B8420416E86B` like this, to get the GPG Key
	```
	gpg --armor --export 3EC4B8420416E86B
	```

5. Paste the GPG key in your Github account [settings](https://github.com/settings/keys)

6. Tell Git about the GPG key you're going to use
	```
	git config --global user.signingkey 3EC4B8420416E86B
	```

{{%panel theme="danger" header="What are GPG Keys?"%}}
GPG Keys allow you to sign your Github commits. They tell github and other users that it's really you, who is committing the change. Learn more about GPG [here](https://help.github.com/articles/about-gpg). A much longer, and detailed, step to create GPG keys is over [here](https://help.github.com/articles/signing-commits-with-gpg/).
{{%/panel%}}
