# Using Patterns #
We currently support 2 special pattern symbols:

`*` - for any sequence of symbols

`_` - for any single symbol


## Examples ##
| **Pattern** | **Matches** | **Not Matches** |
|:------------|:------------|:----------------|
| `*soft.com*` | `http://adserversoft.com, http://microsoft.com` | `http://luxoft.com` |
| `http://adserversoft.com?ref=23_` | `http://adserversoft.com?ref=23a, http://adserversoft.com?ref=234` | `http://adserversoft.com?ref=244` |

## Caveat ##
If you want to use `* or _` as a regular symbol (not special) you cannot simply escape them right now. The behavior is not defined. Let us know if this is important for you and we will make sure escaping works.