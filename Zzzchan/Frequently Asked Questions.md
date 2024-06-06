[Home](https://zzzchan.xyz/index.html)[Boards

+Webring](https://zzzchan.xyz/boards.html)[Overboard](https://zzzchan.xyz/overboard.html)[Account](https://zzzchan.xyz/account.html)

FAQ
===

[\[▼\]](#bottom) [\[▲\]](#top)

| Frequently Asked Questions |
| --- |
| **General**<br><br>* [What is an imageboard?](#whats-an-imageboard)<br>* [What are the rules?](https://zzzchan.xyz/rules.html)<br>* [How can I contact the administration?](#contact)<br><br>**Making posts**<br><br>* [How do names, tripcodes and capcodes work?](#name-formatting)<br>* [What kind of styling options are available when making a post?](#post-styling)<br>* [What is the file size limit?](#post-info)<br><br>**Boards, users & permissions**<br><br>* [How do I make my own board?](#make-a-board)<br>* [What do the board settings for antispam do?](#antispam)<br>* [What is the archive/reverse image search link url format?](#archive-reverse-url-format) |

| [What is an imageboard?](#whats-an-imageboard) |
| --- |
| An imageboard is a type of discussion board where users share images and text about various topics.<br><br>The primary difference between imageboards and traditional forums is that anybody can make a post without registering an account or providing any personal information. This lowers the barrier to entry, protects user identities and focuses on what is said, rather than who says it. |

| [Name formatting](#name-formatting) |
| --- |
| When posting, you can format the name field to include a name, tripcode , capcode, any combination of the three including leaving the field completely blank. Instead of a blank name, "Anonymous" is used, however this depends on board-specific configuration. The optional components are explained below.<br><br>**Format**<br><br>Names should be input like: . Tripcode and capcode are optional components. Please note the whitespace before capcodes is significant.<br><br>Valid examples:<br><br>1. name<br>2. #tripcode<br>3. ##tripcode<br>4. \## capcode<br>5. name#tripcode<br>6. name##tripcode<br>7. name## capcode<br>8. name#tripcode## capcode<br>9. name##tripcode## capcode<br>10. #tripcode## capcode<br>11. ##tripcode## capcode<br>12. ##<br><br>The last example is considered a blank capcode and can be used as a shortcut to display your role. Additionally, if a user has multiple aplicable roles (e.g. a board owner, but the user is also global staff) capcodes will default to their lowest role. To show the higher role, you must be explicit and precede any capcode with the role name e.g. ## Global Staff or ## Global Staff capcode<br><br>Each component can be used in combination or independently. In a post number 9 would look like:<br><br> name !!X8NXmAS44= ##Board Owner capcode 02/08/2019, 09:48:44 [No.](https://zzzchan.xyz/example/thread/1.html#123)[123](https://zzzchan.xyz/example/thread/1.html#postform) HideFilter NameFilter TripcodeModerate<br><br>Hello, world!<br><br>The name appears bold in the top left, followed by the tripcode in regular weight with a !! prefix, then the capcode in a different color, bold and with a ## prefix. The colours may vary between themes but are generally distinct from each other<br><br>**Name**<br><br>The name is simply what name you want to be shown alongside your post. Other users can post with the same name so there is nothing preventing impersonation. This is not related to your username (for registered users).<br><br>**Tripcode**<br><br>A tripcode is a password of sorts, which users can provide in the tripcode component of their name. This tripcode is used in conjunction with a server-known secret to generate a unique\* tripcode portion of the name. Long, unique tripcodes can be used as a form of identity. It is important that you keep tripcodes secret if you use them for some form of identity. A compromised tripcode can be used for impersonation and cannot be revoked in any way. Single # before tripcodes will use the traditional (what is now sometimes known as "insecure") tripcode algorithm shared by many imageboard softwares and websites. Double # before tripcodes will use a sha256 hash with server-side secret for a more secure, non-portable tripcode.<br><br>**Capcode**<br><br>A capcode is a component of the name field only available to authenticated users. This includes admins, global staff, board owners and board staff. If there is no text after the ##, the role will be displayed alone. Leaving a space and putting custom text will be prefixed by the role name. This way, the role is always shown to prevent role impersonation. |

| [Post styling](#post-styling) |     |
| --- | --- |
| Input | Output |
| \>greentext | \>greentext |
| <pinktext | <pinktext |
| \==title== | title |
| ""bold"" | bold |
| \_\_underline\_\_ | underline |
| ~~strikethrough~~ | strikethrough |
| \*\*spoiler text\*\* | spoiler text |
| ''italic'' | italic |
| (((detected))) | ((( detected ))) |
| ##2%9+3 | ![](/file/dice.png)(##2%9+3) = 10 |
| https://example.com | [https://example.com](#!) |
| \[Board Rules\](https://your.imageboard/a/custompage/rules.html)(staff only) | [Board Rules](#!) |
| \>>123 | [\>>123](#!) |
| \>>>/b/ | [\>>>/b/](#!) |
| \>>>/b/123 | [\>>>/b/123](#!) |
| \`inline monospace\` | inline monospace |
| \[code\]language  <br>int main() {...}  <br>\[/code\] | int main() {...} |
| \[code\]aa<br>∧＿∧<br>( ・ω・) Let's try that again.<br>\[/code\] | ∧＿∧<br>( ・ω・) Let's try that again. |
| Supported languages for code block syntax highlighting: [https://github.com/highlightjs/highlight.js/blob/master/SUPPORTED\_LANGUAGES.md](https://github.com/highlightjs/highlight.js/blob/master/SUPPORTED_LANGUAGES.md). If you do not specify a language, a subset of languages is supported for auto-detection: javascript, typescript, perl, js, c++, c, java, kotlin, php, h, csharp, bash, sh, zsh, python, ruby, css, html, json, golang, rust, aa. If the language is "plain", an unsupported value, or the auto-detect confidence is too low, highlighting is disabled for the code block. If the language is "aa", the font will be adjusted for Japanese Shift JIS art. |     |

| [What is the file size limit?](#post-info) |
| --- |
| Max size of form data per-post is 32MB. Because other fields e.g. name, message, etc contribute to this, the maximum size of file uploads will be very slightly smaller than this. |

| [How does moderation work?](#moderation) |
| --- |
| **Local vs. Global reports**<br><br>There exists the concept of "local" and "global" reports. Reporting a post locally will show the post along with reports on the report page for that particular board, and the reports may be actioned upon by the board staff. Reporting a post globally will show the post along with reports on the global manage page available only to global staff and may be actioned upon by global staff. Global reports should be used to flag posts that violate global rules such as illegal content or spam, in contrast to local reports which are for posts that abide by global rules but break board-specific rules (which may be made arbitrarily by board staff). It is also possible to be banned from a board or globally for abuse of the report system.<br><br>**Batch processing of posts**<br><br>Each post has a checkbox in the top left to select it for moderation actions. Multiple posts may be selected to allow batch processing e.g. reporting multiple offending posts in one request. The same is present in moderation interfaces. Some actions for example bans (which are based on IP) may also be handled in batches. Selecting multiple posts and using the ban action will apply a single ban for each unique IP of the selected posts.<br><br>**Time format in moderation interfaces**<br><br>Some moderation interfaces, for example the ban duration when moderating posts, or the ban duration for post filtering use a shorthand for times/length. This format supports years, months, weeks, days, hours, minutes and seconds. An input of "3mo" would mean 3 months and "1y2mo3w4d5h6m7s" would mean 1 year, 2 months, 3 weeks, 4 days, 5 hours, 6 minutes and 7 seconds. Units of time should be in descending order, so "2w1mo" is invalid. However you may use "6w" for example to input 6 weeks, and are not required to use "1mo2w". |

| [How do I make my own board?](#make-a-board) |
| --- |
| [Register](https://zzzchan.xyz/register.html) an account, then please submit a board application as outlined in >>>/meta/137. |

| [What do the board settings for antispam do?](#antispam) |
| --- |
| Lock Mode: Choose to lock posting new threads or all posts.<br><br>Captcha Mode: Choose to enforce captchas for posting threads or all posts.<br><br>PPH Trigger Threshold: Trigger an action after a certain amount of PPH.<br><br>PPH Trigger Action: The action to trigger.<br><br>TPH Trigger Threshold: Trigger an action after a certain amount of TPH.<br><br>TPH Trigger Action: The action to trigger.<br><br>Trigger Reset Lock Mode: If a trigger threshold was reached, reset the lock mode to this at the end of the hour.<br><br>Trigger Reset Captcha Mode: If a trigger threshold was reached, reset the captcha mode to this at the end of the hour.<br><br>Early 404: When a new thread is posted, delete any existing threads with less than 5 replies beyond the first 1/3 of threads.<br><br>Disable anonymizer file posting: Prevent users posting images through anonymizers such as Tor hidden services, lokinet SNApps or i2p eepsites.<br><br>Blocked Countries: Block country codes (based on geo Ip data) from posting. |

| [What do the filter options do?](#filters) |
| --- |
| Filters: Newline separated list of words or phrases to match in posts. Checks name, message, email, subject, and filenames.<br><br>Strict Filtering: More aggressively match filters, by normalising the input compared against the filters.<br><br>Filter Mode: What to do when a post matches a filter.<br><br>Filter Auto Ban Duration: How long to automatically ban for when filter mode is set to ban. Input the duration in time format described in the [moderation section](#moderation). |

| [What is the archive/reverse image search link url format?](#archive-reverse-url-format) |
| --- |
| Put a link with %s where the url of the page/file should go for reverse image search or archive links. For example https://tineye.com/search?url=%s. |

| [How can I contact the administration?](#contact) |
| --- |
| You can email me at [\[email protected\]](https://zzzchan.xyz/cdn-cgi/l/email-protection) |

\- [news](https://zzzchan.xyz/news.html) - [rules](https://zzzchan.xyz/rules.html) - [faq](https://zzzchan.xyz/faq.html) -

[jschan](https://gitgud.io/fatchan/jschan/) 1.4.1