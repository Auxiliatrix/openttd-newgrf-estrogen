# OpenHRT Estrogen
*An OpenTTD full industry replacement set mod with estrogen/testosterone as the end products.*

## Overview
**Features:**<br>
✨ An entirely new industry/cargo set<br>
✨ A mildly accurate industry chain<br>
✨ 17 new industries<br>
✨ 18 new cargoes<br>
✨ FIRS's primary industry supplies mechanic<br>
✨ A new reliability-focused game mechanic<br>

![cargo_flow](https://github.com/user-attachments/assets/993ad0e6-af19-44dc-af1d-29515ea4fdb0)<br>
*New cargo flow*<br><br>


![demo_industries](https://github.com/user-attachments/assets/02757c61-49c4-48a2-bfc9-6b226e1e14e8)<br>
*New industries*<br><br>


![demo_cargo](https://github.com/user-attachments/assets/6cb9db2a-248e-474a-8f63-b84effaa97ce)<br>
*New cargo types*<br><br>


![demo_news_down](https://github.com/user-attachments/assets/626d1af7-896e-4932-b7e0-57c64f3f3557)<br>
*New news*<br><br>


This mod is intended to serve as a full industry replacement set for the game [OpenTTD](https://www.openttd.org/).<br>

While this mod is still currently a work in progress, the gameplay is more or less complete, and is [actively hosted and updated on BaNaNaS](https://bananas.openttd.org/package/newgrf/414b3031).<br>
As such, you can now search for, download, and sync this mod as a NewGRF in the OpenTTD client.<br>

To compile the NewGRF yourself, follow [the installation tutorial](https://www.tt-wiki.net/wiki/NMLTutorial/Installation), and run the following command from the repository's root directory:<br>
`nmlc --grf mygrf.grf mygrf.nml`

## Game Mechanics

### Production Level

![demo_production_half](https://github.com/user-attachments/assets/e9f2884c-5981-4488-a21d-83d829c31773)

In the base game, industries can increase or decrease production based on their monthly `cargo transported` percentage.<br>

This mechanic is similar, but has a few key differences:<br>
1. Industries grow and shrink production based on **consecutive** seasons of good (>60%) or bad (<40%) service.
2. Industry production level is **quantized**, and spans the range of **Minimum**, **Low**, **Default**, **High**, **Very High**, and **Maximum**.
3. At **Minimum** production, industries operate at 25%. At **Maximum** production, industries operate at 338%.
4. Industry production only begins to fluctuate after it has first been serviced.

By utilizing **consecutive** seasons (~3 months) of service, this mod rewards **consistent service without major drops**, encouraging **reliability** instead of just **throughput**.<br>

### Extraction Ratio (Primary Industries)

![demo_primary_half](https://github.com/user-attachments/assets/3880a996-0313-4417-856c-a996ee035ef0)

For those unfamiliar with FIRS's **Engineering Supplies / Farming Supplies** game mechanic, primary industries can have their production boosted by supplying special cargos.<br> 

By delivering **20 crates** of such supplies to the appropriate industry, production is doubled, and then quadruled once **80 crates** have been delivered.<br> 

This boost last for one season, and rewards well-timed distribution of these supplies throughout your network.<br> 

### Conversion Ratio (Secondary Industries)

![demo_secondary_half](https://github.com/user-attachments/assets/a23eb561-4c60-4cd9-9aaf-8db5071eb564)

Instead of an *Extraction Ratio*, **secondary** industries have a **conversion** ratio, which affects the rate at which input cargo is converted into output.<br>
The exact rate varies, but generally, the more **kinds** of input are supplied per season, the more **output per unit of input** the industry will produce.<br>

In this mod, secondary industries produce very little on their own, but their cargo delivery payouts are much higher to compensate, ensuring two things:
1. You can start **anywhere** in the industry chain and still make a decent amount of money.
2. In order to exploit secondary industries to their full potential, you **must** complete their entire industry chain.

This motivates players to expand their networks beyond one single cargo type, and rewards the **breadth** of a network instead of just its **throughput**.

## Final Notes

This mod is currently still very much a work in progress. Game mechanics may be slightly unbalanced, and minor bugs are likely.

In addition, I **do not** recommend you check out the code for this mod. NML is a beautiful nightmare to program in,<br>
but has no method by which to dynamically address a read operation, do any sort of iteration/recursion, or even have<br>
the code available in multiple separate files. I'll get around to refactoring it all eventually™.

### Accreditations:
* Primary industry supplies mechanic blatantly copied from the [FIRS NewGRF by @andythenorth](https://github.com/andythenorth/firs).<br>
* Industry sprites currently frankensteined almagmations available in the base game.

![demo_news](https://github.com/user-attachments/assets/bdae4bb3-3375-4c96-beb0-ce8914262f05)

