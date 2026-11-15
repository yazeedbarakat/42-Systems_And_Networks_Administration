*This activity has been created as part of the 42 curriculum by ybarakat.*

# Net_Practice

## Description

Net_Practice is a networking exercise consisting of 10 levels, each presenting a broken network diagram that must be fixed by correctly configuring IP addresses, subnet masks, and routing tables. The goal is to understand how devices communicate across networks, how subnets are defined and separated, and how routers forward traffic between them.

## Instructions

### Running the training interface

1. Extract the provided archive into any folder of your choice
2. In that folder, run the `run.sh` script — it will launch a local web server and open the interface in your browser
3. If `run.sh` doesn't work, run the following manually:
   ```
   python3 -m http.server 49242
   ```
   Then navigate to `http://localhost:49242` in your browser

### Using the interface

- Enter your intranet login in the field on the welcome screen before starting
- For each level, modify the unshaded (editable) fields until the network functions correctly
- Use the **Check again** button to verify your configuration
- Use the **Get my config** button to export your configuration file once a level is solved
- Click **Next level** to proceed after successfully completing a level

### Exporting and submitting

- Export one configuration file per level using **Get my config** before moving to the next level
- 10 exported configuration files (one per level) must be placed at the root of the repository
- It is important to have your login entered in the interface before exporting, as the files are tied to your login

## Resources

### Networking concepts studied

- **TCP/IP addressing** — how IP addresses are structured and assigned to network interfaces
- **Subnet mask** — how masks define the boundary between the network portion and host portion of an address, and how block sizes are calculated (256 − mask octet = block size)
- **Subnetting** — dividing an address space into smaller networks, calculating network addresses, broadcast addresses, and valid host ranges
- **Default gateway** — the router interface a host forwards packets to when the destination is outside its own subnet
- **Routing tables** — how hosts and routers decide where to send packets based on destination pattern matching (most specific route wins, default route as catch-all)
- **Routers** — devices that connect separate subnets and forward packets between them, with one IP per interface per subnet
- **Switches** — layer 2 devices that connect multiple hosts on the same subnet transparently, with no IP routing involvement
- **OSI model layers** — understanding the distinction between layer 2 (MAC-based switching) and layer 3 (IP-based routing)

### References

- [Kurose & Ross — Computer Networks: A Top-Down Approach](https://gaia.cs.umass.edu/kurose_ross/index.php) — Chapter 4 covers IP addressing and subnetting in depth
- [NetPractice guide by lpaube](https://github.com/lpaube/NetPractice) — level walkthroughs and concept explanations specific to this exercise
- [Professor Messer — Subnetting](https://www.youtube.com/results?search_query=professor+messer+subnetting) — clear visual explanation of subnet mask math
- [Cloudflare — What is a routing table?](https://www.cloudflare.com/learning/network-layer/what-is-a-routing-table/) — explains routing table logic and longest-prefix match

### AI usage

Claude (claude.ai) was used during this activity as a learning aid — specifically to explain concepts such as how subnet masks define block boundaries, why mismatched masks cause asymmetric routing failures, how routing tables match destination patterns, and why loopback addresses (`127.x.x.x`) cannot be assigned to real interfaces. AI was not used to directly provide level solutions; reasoning through each level was done independently with AI used only to clarify underlying concepts when stuck.
