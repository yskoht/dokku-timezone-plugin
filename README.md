Original repository is [udzura/dokku-timezone-plugin](https://github.com/udzura/dokku-timezone-plugin).

---

dokku-timezone-plugin
=====================

A plugin to set timezone on buildstep image created

## Install

```bash
$ dokku plugin:install https://github.com/yskoht/dokku-timezone-plugin
```

* Detecting timezone via `/etc/timezone` on dokku host.

```shell-session
[shell]$ git push dokku master
Counting objects: 1, done.
Writing objects: 100% (1/1), 188 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
remote: Cloning into '/tmp/tmp.pUIXrBCKAg'...
-----> Cleaning up ...
-----> Building sample ...
remote: done.
remote: HEAD is now at 5e23906... To deploy
-----> Setting up timezone
-----> Timezone is set to Asia/Tokyo
...
```

## Setting

This plugin detects timezone via `/etc/timezone` by default.

If you want to customize default timezone, please set `${DOKKU_ROOT:=/home/dokku}/dokkurc` below:

```
export TIMEZONE=Asia/Tokyo
```

## Note

This plugin requires `/etc/timezone` file. So may work well onlly on Ubuntu/Debian.

