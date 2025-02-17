﻿# 🧃 Filtered Cola - L08 C07

Hey recruit, back on the previous level you might have been involved with the team that was looking into one of The Chiquitoos' side businesses: the bottling plant. We found their price list request form was vulnerable to command injection and we think the site must also be open to SQL injection.

On the site there's a page where you can search through a list of all the orders they are planning to fulfil over the next month and we've got you access to it. We think that some of the results are hidden and only available to the senior gang members. We need that extra list so we can see when they are planning to re-label the stolen Cola as a different brand.

One of our other agents has already tried but, unfortunately, it looks like there is a filter being applied to prevent certain phrases being used in the form. Can you bypass it?

**Tip:** Get the full list and you'll also get the flag. The flag is the name of the handler on the last result marked "secret".

<details><summary>

## Need a hint?</summary>

> 💡 Hint: Hmm, it seems the filter is just for 1=1. Is there another way to accomplish the same thing?

</details>

<details><summary>

## Step by Step</summary>

- Enter `anything' OR 2=2 -- //` in the search bar
- Scroll down until the first `Secret` status
- The name of the handler is the flag

![image of search result](/assets/filteredcola1.jpg)

</details>
