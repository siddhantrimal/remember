+++
title= "Setting Up Git With SSH"
date= 2017-11-10T16:37:33+05:45
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

1. First check existing SSH keys<sup>[1]</sup>

	```
	ls -al ~/.ssh
	```

2. Then generate one, if necesary<sup>[1]</sup>
	
	```
	ssh-keygen -t rsa -b 4096 -C "siddhantrimal@hotmail.com"
	```

	to store this in the global context, provide this filepath:
	```
	/c/Users/Siddhant/.ssh/id_rsa
	```

3. Copy the SSH key to clipboard<sup>[2]</sup>
	```
	clip < ~/.ssh/id_rsa.pub
	```

	Now login to your github account and, while logged in, open [this link][3] `https://github.com/settings/keys` on the next tab and paste the key from your clipboard. Henceforth, use the SSH address of your repository to use it.

[1]: https://help.github.com/articles/checking-for-existing-ssh-keys/
[2]: https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
[3]: https://github.com/settings/keys