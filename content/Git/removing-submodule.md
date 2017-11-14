+++
title= "Removing Submodule"
date= 2017-11-14T23:35:22+05:45
description = "How to remove submodule in git"
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

1. Remove the submodule entry from `.git/config`<sup>[1]</sup>
```
git submodule deinit -f path/to/submodule
```

2. Remove the submodule directory from the superproject's `.git/modules` directory<sup>[1]</sup>
```
rm -rf .git/modules/path/to/submodule
```

3. Remove the entry in `.gitmodules` and remove the submodule directory located at path/to/submodule<sup>[1]</sup>
```
git rm -f path/to/submodule
```

4. Remove cached entries; Delete `.gitmodules` before doing this, if it hasn't deleted already<sup>[2]</sup>
```
rm -rf path/to/submodule
```

[1]: https://stackoverflow.com/a/36593218
[2]: https://stackoverflow.com/a/7646931
