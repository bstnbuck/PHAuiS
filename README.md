**P**assword **H**ashing **A**lgorithms **u**sed **i**n **S**oftware pronounced as `[faus]` (with a silent *i*) is a simple overview of password hashing algorithms used in software with authentication capabilities. 

👉The goal is to evaluate the security of the algorithms used in the respective program.


## PHAuiS🔑

:grey_question: **Rating** is based on:<br>
<sub>\* in combination with another symbol</sub>

* **Currently one of the best***: :heavy_check_mark:
* **Good but not perfect**: :green_circle:
* Moderate: :yellow_circle:
* *Bad*: :red_circle:
* *Couldn't be worse**: :x:

<details>
<summary>
<b>Overview about typical algorithms and their rating</b>
</summary>

| PH-Algorithm | Rating | Explanation |
| --- | --- | --- |
| **Argon2(i/d/id)** <sub>(with/without Salt)</sub> | :green_circle::heavy_check_mark: | State-of-the-Art (Winner of Password Hashing Competition) [[1](https://www.password-hashing.net/)] [[2](https://github.com/P-H-C/phc-winner-argon2/blob/master/argon2-specs.pdf)] [[Git](https://github.com/p-h-c/phc-winner-argon2)] |
| Yescrypt <sub>(with/without Salt)</sub> | :green_circle::heavy_check_mark: | Password Hashing Competition finalist with special recognitions [[1](https://www.password-hashing.net/)] [[2](https://www.openwall.com/yescrypt/)]  |
| Catena <sub>(with/without Salt)</sub> | :green_circle::heavy_check_mark: | kind of scrypt, Password Hashing Competition finalist with special recognitions [[1](https://www.password-hashing.net/)] [[2](https://eprint.iacr.org/eprint-bin/getfile.pl?entry=2013/525&version=20130830:084400&file=525.pdf)]  |
| Lyra2 <sub>(with/without Salt)</sub> | :green_circle::heavy_check_mark: | Password Hashing Competition finalist with special recognitions [[1](https://www.password-hashing.net/)] [[2](https://ieeexplore.ieee.org/document/7377075)]  |
| Makwa <sub>(with/without Salt)</sub> | :green_circle::heavy_check_mark: | Password Hashing Competition finalist with special recognitions [[1](https://www.password-hashing.net/)] [[2](https://www.bolet.org/makwa/)]  |
| Pufferfish <sub>(with/without Salt)</sub> | :green_circle: | kind of blowfish, Password Hashing Competition finalist [[1](https://www.password-hashing.net/submissions.html)] [[2](https://github.com/epixoip/pufferfish)] |
| bcrypt <sub>(with/without Salt)</sub> | :green_circle: | kind of blowfish, crypt ($2a), [[1](https://www.usenix.org/legacy/events/usenix99/provos/provos.pdf)] [[2](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html)] |
| scrypt <sub>(with/without Salt)</sub> | :green_circle: | [[1](https://www.tarsnap.com/scrypt/scrypt.pdf)] [[2](https://datatracker.ietf.org/doc/html/rfc7914)] |
| PBKDF2 <sub>(with Salt and/or high key-stretching)</sub> | :green_circle: | [[1](https://web.archive.org/web/20170411220929/https://www.emc.com/collateral/white-papers/h11302-pkcs5v2-1-password-based-cryptography-standard-wp.pdf)] [[2](https://datatracker.ietf.org/doc/html/rfc2898)] [[3](https://mathiasbynens.be/notes/pbkdf2-hmac)]|
| SHA2/3 <sub>(with Salt and/or key-stretching)</sub> | :green_circle: | crypt (\$5, $6), [[1](https://man7.org/linux/man-pages/man3/crypt.3.html)] |
| Blake2b <sub>(with Salt and/or key-stretching)</sub> | :green_circle: | [[1](https://www.blake2.net/)] |
| PBKDF2 <sub>(without Salt and with high key-stretching)</sub> | :yellow_circle::green_circle: | |
| SHA2/3 512 bit <sub>(without Salt)</sub> | :yellow_circle::green_circle: |  |
| Blake2b 512 bit <sub>(without Salt)</sub> | :yellow_circle::green_circle: |  |
| SHA2/3 256 bit <sub>(without Salt)</sub> | :yellow_circle: | |
| RIPEMD-160 <sub>(with Salt and/or key-stretching)</sub> | :red_circle::yellow_circle: | [[1](https://link.springer.com/chapter/10.1007/978-3-031-30634-1_7)] [[2](https://homes.esat.kuleuven.be/~bosselae/ripemd160/pdf/AB-9601/AB-9601.pdf)] |
| SHA1 <sub>(with Salt and/or key-stretching)</sub> | :red_circle::yellow_circle: | collission + length extension attacks [[1](https://www.schneier.com/blog/archives/2005/02/sha1_broken.html)] [[2](http://people.csail.mit.edu/yiqun/SHA1AttackProceedingVersion.pdf)] [[3](https://eprint.iacr.org/2019/459.pdf)] |
| MD5 <sub>(with Salt and/or key-stretching)</sub> | :red_circle::yellow_circle: | crypt ($1), collission + length extension attacks [[1](https://eprint.iacr.org/2013/170.pdf)] [[2](https://www.zdnet.com/article/a-quarter-of-major-cmss-use-outdated-md5-as-the-default-password-hashing-scheme/)] |
| RIPEMD-160 <sub>(without Salt)</sub> | :red_circle: |  |
| SHA1 <sub>(without Salt)</sub> | :red_circle: |  |
| MD5 <sub>(without Salt)</sub> | :red_circle: |  |
| GOST <sub>(without Salt)</sub> | :red_circle: | collission + preimage attacks [[1](https://link.springer.com/chapter/10.1007/978-3-540-85174-5_10)] |
| MD4 <sub>(without/with Salt and/or key-stretching)</sub> | :red_circle::x: | Rainbow Tables available, Collission Attacks [[1](https://www.iacr.org/archive/fse2007/45930331/45930331.pdf)] |
| NTLM-Hash | :red_circle::x: | Based on MD4 without key-stretching, Salt, ..., [[1](https://learn.microsoft.com/en-us/windows-server/security/kerberos/passwords-technical-overview)] |
| DES | :red_circle::x: | obsolete Encryption-Algorithm, [[1](https://web.archive.org/web/20140226205104/http://origin-www.computer.org/csdl/mags/co/1977/06/01646525.pdf)] |
| LM-Hash | :red_circle::x: | Rainbow Tables available, Collission Attacks, [[1](https://learn.microsoft.com/en-us/windows-server/security/kerberos/passwords-technical-overview)] [[2](https://learn.microsoft.com/en-us/troubleshoot/windows-server/windows-security/prevent-windows-store-lm-hash-password)] |
| CRC32 | :red_circle::x: | just a error-detecting code |
| General: Any Encryption Algorithm | :red_circle: | Encryption Key is somewhere on the system?!? |
</details>

---

**Web-Applications / Software**

| Program name | Versions | PH-Algorithm &rarr; Rating | Sources | Extras |
| --- | --- | --- | --- | --- |
| Aegis | all | scrypt  &rarr; :green_circle: | [[1](https://github.com/beemdevelopment/Aegis)] | |
| Bitwarden, Vaultwarden | all | PBKDF2 <sub>(with Salt and/or key-stretching (default: 600.000))</sub> &rarr; :green_circle: <br> or Argon2id <sub>(64MiB, 3 times, 4 threads)</sub> &rarr; :green_circle::heavy_check_mark: | [[1](https://bitwarden.com/de-DE/help/kdf-algorithms/)], [[2](https://github.com/dani-garcia/vaultwarden/blob/main/src/db/models/user.rs#L66)] | Salt is username/e-mail |
| CheckMK | >2.1.0p16 >2.2.0b1  | bcrypt <sub></sub> &rarr; :green_circle: <br> SHA256 <sub>(with Salt and/or key-stretching)</sub> &rarr; :green_circle: | [[1](https://checkmk.com/werk/14391)] | |
| CheckMK | <=2.1.0p16 <=2.2.0b1  | DES &rarr; :red_circle::x: <br> MD5 <sub>(with Salt and/or key-stretching)</sub> &rarr; :red_circle::yellow_circle: <br> SHA256 <sub>(with Salt and/or key-stretching)</sub> &rarr; :green_circle: | [[1](https://checkmk.com/werk/14391)] | |
| Drupal | all | based on PHP password_hash() (default: bcrypt) &rarr; :green_circle: | [[1](hhttps://www.drupal.org/node/3322420)] | |
| FileGator | all | bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: | [[1](https://github.com/filegator/filegator/blob/master/backend/Utils/PasswordHash.php)] | |
| Gitea | all | bcrypt, scrypt, PBKDF2 <sub>(with Salt)</sub> &rarr; :green_circle: <br> Argon2 <sub>with Salt, time=2, memory=64*1024, threads=8, keyLen=50</sub> &rarr; :green_circle::heavy_check_mark: | [[1](https://github.com/go-gitea/gitea/tree/main/modules/auth/password/hash)] | |
| Gophish | all | bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: | [[1](https://github.com/gophish/gophish/blob/master/auth/auth.go#L48)] | |
| ILIAS e-Learning | >5.(0,1,2).X  | bcrypt <sub>(with/without Salt)</sub> &rarr; :green_circle: | [[1](https://docu.ilias.de/goto_docu_wiki_wpage_4198_1357.html)] | |
| ILIAS e-Learning | <5.(0,1,2).X  | MD5 <sub>without Salt</sub> &rarr; :red_circle: | [[1](https://docu.ilias.de/goto_docu_wiki_wpage_4198_1357.html)] | |
| ISPconfig | all | crypt <sub>Linux defaults</sub> &rarr; :red_circle::yellow_circle: or :green_circle:|  |  |
| Joomla  | >4.0.0 |  MD5 <sub>(without Salt)</sub> &rarr; :red_circle: <br> bcrypt (default) &rarr; :green_circle: <br> Argon2(i, id) &rarr; :green_circle::heavy_check_mark: | [[1](https://github.com/joomla/joomla-cms/blob/4.4-dev/libraries/src/User/UserHelper.php)] | |
| KeePass | >2.X | AES-KDF &rarr; :red_circle: <br> Argon2(d, id) &rarr; :green_circle::heavy_check_mark: | [[1](https://keepass.info/help/base/security.html)] |  |
| LastPass | - | PBKDF2 <sub>key-stretching 100.100</sub> &rarr; :green_circle::heavy_check_mark: | [[1](https://blog.lastpass.com/2022/12/notice-of-recent-security-incident/)] | |
| LDAP | ? | SHA1, MD5 <sub>with and without Salt</sub> &rarr; :red_circle:, :red_circle::yellow_circle: <br> Linux crypt(3) (MD5, Blowfish, SHA2 (256, 512 bit)) <sub>with Salt and Key stretching</sub> &rarr; :red_circle::yellow_circle: up to :green_circle: | [[1](https://www.openldap.org/doc/admin24/security.html)] [[2](https://man7.org/linux/man-pages/man3/crypt.3.html)] [[3](https://www.rfc-editor.org/rfc/rfc4519.txt)] | official RFC specifies no encryption/hash |
| MySQL | <4.1  | custom 16 Byte construct (broken) &rarr; :red_circle::x: | [[1](https://dev.mysql.com/blog-archive/protecting-mysql-passwords-with-the-sha256_password-plugin/)] | |
| MySQL/MariaDB mysql_native_password (default plugin) | > MySQL 4.1  | SHA1 construct <sub>with Salt and minimal key-stretching</sub> &rarr; :red_circle::yellow_circle: | [[1](https://mariadb.com/kb/en/authentication-plugin-mysql_native_password/)], [[2](https://dev.mysql.com/doc/refman/5.7/en/password-hashing.html)] | low key-stretching value, better algorithms available (ed25519 based, sha256 construct) [[3](https://mariadb.com/kb/en/authentication-plugin-ed25519/)] but not default, [[4](https://dev.mysql.com/blog-archive/protecting-mysql-passwords-with-the-sha256_password-plugin/)], this algorithm can be exploited [[5](https://github.com/cyrus-and/mysql-unsha1)] |
| Nextcloud | all | bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: | [[1](https://docs.nextcloud.com/server/latest/admin_manual/installation/harden_server.html#limit-on-password-length)] | |
| ownCloud core | all | bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: | [[1](https://doc.owncloud.com/server/next/admin_manual/configuration/server/harden_server.html#limit-on-password-length)] | |
| PI-hole | all | SHA2 256 bit <sub>without Salt, key-stretching 2x</sub> &rarr; :yellow_circle: | [[1](https://github.com/pi-hole/web/blob/master/scripts/pi-hole/php/password.php#L42)] | |
| Prestashop  | all |  MD5 <sub>(with Salt)</sub> &rarr;:red_circle: | [[1](https://github.com/PrestaShop/PrestaShop/blob/develop/src/Core/Security/Hashing.php)] | |
| Typo3 | all | MD5 <sub>(with Salt)</sub> &rarr; :red_circle: <br> blowfish, phpass<sub>(with password stretching)</sub> &rarr; :red_circle: <br> PBKDF2, bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: <br> Argon2(i, id) &rarr; :green_circle::heavy_check_mark: | [[1](https://github.com/h44z/wg-portal/blob/master/internal/domain/user.go#L127)] | |
| Slack | - | SHA256 <sub>(with Salt)</sub> &rarr; :green_circle: | [[1](https://news.sophos.com/en-us/2022/08/08/slack-admits-to-leaking-hashed-passwords-for-three-months/)] | |
| urbackup | all | PBKDF2 with SHA512 <sub>Internet-User secret; without Salt, key-stretching 20.000</sub> &rarr; :yellow_circle::green_circle: <br> PBKDF2 with MD5 <sub>Login-User; with Salt, key-stretching >0</sub> &rarr; :yellow_circle:| [[1](https://www.urbackup.org/administration_manual.html#x1-250004.5)] [[2](https://github.com/uroni/urbackup_backend/blob/dev/urbackupserver/serverinterface/helper.cpp#L319)] | low key-stretching value|
| wg-portal | all | bcrypt <sub>(without Salt)</sub> &rarr; :green_circle: | [[1](https://github.com/h44z/wg-portal/blob/master/internal/domain/user.go#L127)] | |
| Wordpress  | all |  MD5 <sub>(with Salt + minimal key stretching)</sub> &rarr; :red_circle: | [[1](https://developer.wordpress.org/reference/functions/wp_hash_password/)] | better algorithms just like Argon2id available with Plugins |

**Operating Systems**
| Program name | Versions | PH-Algorithm &rarr; Rating | Sources | Extras |
| --- | --- | --- | --- | --- |
| Linux (Debian, Ubuntu) | variable |  DES &rarr; :red_circle::x:<br> MD5, SHA1 <sub>(with Salt and/or key-stretching)</sub> &rarr; :red_circle::yellow_circle: <br> bcrypt, scrypt, SHA256, SHA512 <sub>(with Salt and/or key-stretching)</sub> &rarr; :green_circle: <br> (gost-)yescrypt <sub>(with Salt)</sub> &rarr; :green_circle::heavy_check_mark:| [[1](https://man7.org/linux/man-pages/man3/crypt.3.html)] [[2](https://manpages.debian.org/testing/libcrypt-dev/crypt.5.en.html)] | based on current Debian specification |
| Windows | <Vista |  LM-Hash &rarr; :red_circle::x: <br> NTLM-Hash &rarr; :red_circle::x:| [[1](https://learn.microsoft.com/de-de/troubleshoot/windows-server/windows-security/prevent-windows-store-lm-hash-password)] | |
| Windows | >=Vista |  NTLM-Hash &rarr; :red_circle::x: | [[1](https://learn.microsoft.com/de-de/troubleshoot/windows-server/windows-security/prevent-windows-store-lm-hash-password)]| |


> Last Update: 19-02-2024
