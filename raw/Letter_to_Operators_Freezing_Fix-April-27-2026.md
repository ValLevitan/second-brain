April 27, 2026

**\
Re: Flex cabinet freezing --- root cause identified and free upgrade**

Dear Operator,

I am writing to you directly because what we have to share is important, and because I prefer you hear it from me in plain terms rather than through a marketing document.

**What we found**

On a portion of the Flex cabinets in the field, revenue has been running below where it should be. The natural reading --- and for some time it was ours as well --- was that the software was simply earning less. It was not.

The machines were freezing. A frozen cabinet is not a cabinet that is underperforming; it is a cabinet that is sitting out of service and earning nothing. The individual freezes that did get reported were treated as isolated incidents. The cumulative downtime they were causing, and the revenue impact of that downtime, was not visible to you or to us.

**Why a problem like this can hide in plain sight**

I want to be direct about something, because it matters more than the freeze itself. The reason an issue of this scale can exist across a fleet, in your hands and in ours, and not surface for what it actually is, is that the industry today operates without a culture or an infrastructure for tracking the health of connected machines. Operators run blind. Manufacturers run blind. The only signal anyone gets is when a technician happens to be standing in front of a frozen cabinet at the right moment, and that signal almost never makes it back to the people who could act on it.

That has to change, and it is something JVL is actively working on. Our goal --- and we are investing real engineering effort behind it --- is to make cabinet health information discoverable, in real time, by every operator on every EGM. When that capability exists, problems like this one surface in days, not in months of inferred revenue patterns.

**The cause**

The diagnostic work of the past months was the hard part. This was not a problem that announced itself in a logfile. It lived in the gap between the cabinet hardware, the operating-system kernel, and the graphics subsystem, and we had to rule out several plausible alternatives before we got to the right answer.

What we found is an incompatibility between the integrated graphics processor on the affected cabinet platforms and the Linux operating kernel they were running (version 4.19). Under sustained graphics load --- for example during bonus rounds --- the combination would, on occasion, lock the machine up completely, requiring a power cycle to recover. The motherboard vendor independently confirmed in writing that the kernel we were shipping was not appropriate for that processor and pointed us to the current long-term-support release.

I will say plainly that I am proud of the team that ran this down. This is the kind of problem that disappears in many engineering organizations because nobody wants to chase it through three layers of the stack. Our team did, and we have it.

**\
The fix**

We have upgraded the operating kernel to version 5.15 LTS, the current long-term-support release recommended for this hardware. Across the initial production deployments --- including a controlled set of cabinets that have now been running for several weeks --- the freezing has not recurred. We are continuing to monitor as the upgrade rolls out more broadly, and the root cause is, in our judgment, correctly identified and the fix sound.

**Why this matters to your bottom line**

The value of this fix is uptime, and uptime is cash. Picture it concretely. If a cabinet has been down half the time it should have been running, restoring it does not give you a 50% lift --- it gives you more than that. The hours you recover are not random hours; they are the hours when a player walked up, found a frozen screen, and walked away. Those are your peak earning hours, hour for hour. Every dollar of that recovered revenue goes directly to your bottom line. No new investment. No commercial obligation. No contract. It is simply cash in your pocket --- money that was already yours, sitting on the table, waiting on the cabinet to come back online so you could collect it.

**What we are doing**

Because of the trust you have placed in us and the business we have built together, we are not charging for this upgrade. The software, which we ordinarily sell for \$2,500 per cabinet, will be provided to you at no cost for every affected unit in your fleet.

Felipe Miranda Giorgi will be in touch with the specific serial numbers we have on file against your account. He will ask you to confirm which of those cabinets are still in your possession and to coordinate the installation schedule. I ask only two things of you in return:

1.  **Act on this promptly.** Every cabinet that remains on the old kernel is a cabinet leaving revenue on the table.

2.  **Provide the COM ID at the time of each installation.** This is how we confirm the upgrade landed on the machine it was intended for, and how we track that the fix is holding in the field. It is also the first practical step toward the broader visibility I described above --- when we know which cabinet is running which build, we can see when something is going wrong on it instead of inferring it after the fact.

Sincerely,

**Val Levitan**

JVL
