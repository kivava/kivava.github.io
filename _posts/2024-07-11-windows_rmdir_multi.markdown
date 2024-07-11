---
layout: posts
title:  "Remove multiple folders on Windows"
date:   2024-07-09 17:00:00 +0800
categories: jekyll
---
Remove multiple folders on Windows

## CMD to remove multiple folders
```
for /D %f in (output*) do @rmdir "%f" /Q /S
```


## Reference:

[Delete several directories with a common prefix at the command prompt](https://superuser.com/questions/691072/delete-several-directories-with-a-common-prefix-at-the-command-prompt)