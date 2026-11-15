# Mission 7 — How computers communicate

## 1. Task / objective

Explain basic network concepts, observe connectivity and DNS information, and describe what happens when a browser opens a website.

## 2. Work completed

### Task 7.1 — Network concepts

| Concept | Explanation | Example |
|---|---|---|
| LAN | A network connecting devices across a small area | A home or computer-lab network |
| MAN | A network covering a metropolitan area | A network connecting municipal offices across a city |
| WAN | A network connecting locations across large geographical areas | A company network linking offices in different countries |
| DNS | Resolves domain names to records, including IP addresses | Looking up the address for `example.com` |
| Router | Forwards packets between networks | A home router connecting a local network to an ISP |
| Protocol | Agreed rules for communication | HTTP for web requests and responses |
| Packet switching | Sends information as packets across shared network links | Transferring a file over the internet |
| Client-server | A client requests a service and a server responds | A browser requesting a webpage from a web server |

### Task 7.2 — Observe network information

Connectivity command:

```bash
ping -c 4 example.com
```

This sends four ICMP echo requests and reports responses if they arrive.

Actual observation:

- Replies received: 4 out of 4.
- Packet loss: 0.0%.
- Approximate response time: 41.77 ms on average.

A connectivity test helps check whether a destination responds to a particular type of network traffic. A failed ping does not prove that a website is unavailable because ICMP traffic may be blocked.

DNS command:

```bash
nslookup example.com
```

Actual observation:

- Lookup succeeded or failed: Succeeded.
- Record/address types displayed: Two IPv4 addresses (A records) for `example.com`: `104.20.23.154` and `172.66.147.243`.

A DNS lookup displays information associated with a domain, such as IPv4 or IPv6 addresses. The output may also identify the DNS server used for the lookup.

DNS helps the browser obtain an address for a website name. Cached results may sometimes be used instead of a new lookup.

Private network details and identifying information are excluded from the published observations.

### Task 7.3 — What happens when a website opens?

1. I enter a URL into a browser. The browser acts as the client.
2. The browser or operating system obtains the destination address using DNS or a cached result.
3. The device sends network traffic through the local network and router towards the destination.
4. For an HTTPS website, the client establishes a secure connection using the required transport and security protocols.
5. The browser sends an HTTP request asking the server for a resource.
6. The server sends a response, and the data is transported across the network in packets.
7. The browser processes the returned resources and displays the page. It may send additional requests for images, stylesheets or scripts.

This is a simplified sequence. Caching can avoid some network requests.

## 3. Commands / tools used

| Command / tool | Purpose |
|---|---|
| `ping -c 4 example.com` | Test for responses using four echo requests |
| `nslookup example.com` | Inspect DNS information for the domain |
| Terminal | Run network commands |
| VS Code | Record explanations and safe observations |
| Git and GitHub | Commit and publish the mission |

## 4. My understanding

A network allows devices to exchange data and share resources.

DNS helps translate human-readable website names into information that computers use to find destinations. Routers forward packets between networks.

Protocols provide communication rules. In client-server communication, the client requests something and the server responds.

## 5. Difficulties faced

 No major difficulties. I received all four ping replies, and the DNS lookup returned two IPv4 addresses for `example.com`.

## 6. How I resolved them

 Not applicable.
## 7. Evidence / files

- `mission-07-networking/README.md`.
- Network-concepts table.
- Actual privacy-safe connectivity and DNS observations.
- Seven-step website explanation.

## 8. Commit details

Planned commit message: `Explain networking concepts and website communication`

Commit, push and GitHub verification: [I committed the Mission 7 work with the message `Explain networking concepts and website communication` and pushed it to `main`. I opened the README on GitHub and verified that my network concepts table, ping and DNS results, and six-step website explanation were visible.]