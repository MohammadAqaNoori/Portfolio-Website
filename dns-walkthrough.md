# DNS Walkthrough — Personal Portfolio Website

## 1. What DNS does

DNS (Domain Name System) translates a human-readable domain name into information that allows a browser to find the correct server hosting a website.

For example, when someone enters `maqanoori.netlify.app` into a browser, DNS helps the browser determine where the website is hosted so that it can request the site's files.

## 2. What a CNAME record is

A CNAME (Canonical Name) record is a DNS record that points one domain or subdomain to another hostname.

For a future FlyRank subdomain, for example:

- **Name/Host:** `maqanoori`
- **Type:** `CNAME`
- **Target:** the hostname provided by the hosting platform or FlyRank Ops

The exact target value depends on the DNS instructions provided when the FlyRank subdomain is provisioned.

A CNAME does not contain the website itself. It tells DNS where the requested hostname should be directed.

## 3. What happens when someone visits the website

When a user enters a domain name into a browser, several steps happen:

1. The browser needs to find the IP address or hosting destination associated with the domain.
2. The DNS resolver receives the request and looks for the required DNS information.
3. If the resolver does not already have the answer cached, it communicates with the appropriate DNS nameservers.
4. The nameserver returns the relevant DNS record, such as a CNAME or an address record.
5. The resolver returns the result to the browser.
6. The browser uses that information to connect to the hosting service.
7. The hosting service responds with the website files.
8. Because the site is served over HTTPS, the browser also establishes a secure encrypted connection before transferring the website content.

## 4. My current hosting setup

My portfolio website is currently hosted on Netlify and is publicly available over HTTPS at:

`https://maqanoori.netlify.app/`

The Netlify-hosted URL is the current public address for the portfolio.

The website does not require a custom DNS configuration from me for the Netlify-provided subdomain because Netlify manages the DNS relationship for that hosted address.

## 5. Future FlyRank subdomain

The internship brief states that a FlyRank subdomain will be provisioned after the capstone is approved.

When that happens, the expected process is:

1. Receive the assigned FlyRank subdomain and DNS target from FlyRank Ops.
2. Add the custom domain in the hosting provider's domain settings.
3. Configure the required DNS record using the exact target supplied by FlyRank Ops.
4. Wait for DNS propagation.
5. Verify that the domain resolves to the portfolio website.
6. Confirm that HTTPS is active and the browser shows a secure connection.

The exact CNAME target should not be guessed. It should be copied from the instructions provided by FlyRank Ops or the hosting provider at the time the subdomain is provisioned.

## 6. DNS propagation

After a DNS record is changed, the change may not appear immediately everywhere because DNS information can be cached by resolvers.

This period is called DNS propagation. During propagation, some users may temporarily receive the previous DNS information while others receive the updated record.

I would therefore verify the new domain after the DNS change rather than assuming that the configuration is immediately active.

## 7. Summary

The important distinction is that DNS is responsible for directing a domain name to the appropriate hosting destination, while the hosting platform serves the actual website.

My current portfolio is hosted at `maqanoori.netlify.app`. When the FlyRank subdomain becomes available, I will add that custom domain to the hosting provider, configure the required DNS record using the supplied target, wait for propagation, and verify that the website is available securely over HTTPS.
