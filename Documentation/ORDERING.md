# Ordering the Click Me circuit board

This guide orders the Click Me printed circuit board (PCB) from JLCPCB, with the
two electronic parts already soldered on. You do not solder anything.

The board is small and simple: a 3.5 mm mono jack and a socket that a mechanical
keyboard switch clicks into. Everything else about the device is 3D printed.

Read [ASSEMBLY.md](ASSEMBLY.md) for what to do once the boards arrive.

> **Status: work in progress.** These are the settings used for the boards in the
> photos, ordered in July 2026. JLCPCB changes its website, its option names and
> its prices. Treat every screen name below as "look for something like this"
> rather than an exact match, and check the preview before you pay.

## 1. What you need before you start

Three files from this repository, all in
[`Build_Files/PCB_Build_Files/`](../Build_Files/PCB_Build_Files):

| File | What it is |
|---|---|
| `Gerber_PCB1_2026-09-21.zip` | The board itself: copper, holes, outline |
| `BOM_ClickMe.csv` | The parts list: which components to solder |
| `CPL_ClickMe.csv` | Where each component sits and which way round |

Download all three. Do not unzip the Gerber file; JLCPCB wants the `.zip`.

You also need a JLCPCB account, and a payment method.

## 2. Upload the board file

1. Go to [jlcpcb.com](https://jlcpcb.com).
2. Select **Add gerber file** and choose `Gerber_PCB1_2026-09-21.zip`.
3. Wait for the preview to appear.
4. **Check the preview before going further.** You should see a small square board
   with two rounded mounting slots and one square outline near the middle. The
   dimensions should read about **46 x 46 mm (1.81 x 1.81 in)**. If the size is
   wildly different, or the preview is blank, the upload failed. Try again rather
   than continuing.

## 3. Board options

These are the options used for the boards in the photos. Where a name has changed,
pick the nearest equivalent.

| Option | Value | Why |
|---|---|---|
| Layers | 2 | What the design uses |
| Dimensions | filled in automatically | From the board file |
| PCB thickness | 1.6 mm | Standard; the printed housing is sized for it |
| PCB material | FR-4 | Standard fibreglass board |
| Outer copper weight | 1 oz | Standard |
| Surface finish | Lead-free HASL | Standard, and no lead |
| Solder mask | Purple | Cosmetic only; pick any colour you like |
| Silkscreen | White | Cosmetic only |
| Via covering | Tented | Standard |
| Minimum hole size | 0.3 mm | Standard, no extra charge |
| Remove order number | leave at the default | Cosmetic only |

Everything not listed can stay at its default.

**Quantity.** The form has a minimum, normally 5 boards. Building one Click Me
needs one board, so you will have spares whatever you choose. A bigger batch is
dramatically cheaper per board, because so much of the cost is charged once per
order. Even so, read section 8 before you size your order, because cheaper per board
is not the same as the right number to buy.

## 4. Turn on assembly

This is the step that makes the board solderless for you.

1. Switch **PCB Assembly** on.
2. Set the assembly side to the **top side** only.
3. Set how many of your boards to have assembled. This can be fewer than the
   number of bare boards, and assembled boards cost more than bare ones.
4. Continue to the parts upload step.

**Economic or Standard?** JLCPCB offers tiers under different names. Economic is
cheaper and covers ordinary surface-mount parts, which is all this board has.
Standard costs more and handles a wider range of parts. The batch in the photos
was made as Standard. With only two surface-mount parts on one side, Economic may
well be offered and accepted. Pick whichever the form allows for your upload, and
if only one tier is offered, take it.

## 5. Upload the parts list and positions

1. Upload `BOM_ClickMe.csv` where it asks for the **BOM** or parts list.
2. Upload `CPL_ClickMe.csv` where it asks for the **CPL**, **pick and place**, or
   **component placement** file.
3. Continue to the parts confirmation screen.

**You should see exactly two parts:**

| Designator | Part | LCSC part number | What it is |
|---|---|---|---|
| CN1 | PJ-320B | C22355831 | The 3.5 mm mono jack your cable plugs into |
| U1 | CPG151101S11-16 | C41430893 | The socket the keyboard switch clicks into |

If a **third** part appears, or a part number differs from the table, stop and
check you uploaded the files from this repository. The mechanical keyboard switch
is deliberately not in these files. You buy that separately, and paying JLCPCB to
fit one would defeat the point of a hot-swap socket.

If either part shows as out of stock, JLCPCB will offer a substitute. A different
3.5 mm mono jack in the same PJ-320B footprint is usually fine. For the socket,
any Kailh-compatible MX hot-swap socket in the same footprint is usually fine.
Read the substitute's dimensions before accepting it.

## 6. Review and order

1. Work through the remaining screens: shipping, customs, and payment.
2. Before paying, check the summary shows the board quantity, the assembled
   quantity, and two parts.
3. Place the order.

Boards typically take a few weeks including shipping. JLCPCB will send your order
through an engineering review and may email a question; answering it promptly
avoids a delay.

## 7. What arrives, and what you still need

**In the parcel:** your bare boards, and your assembled boards with the jack and
the socket already soldered on.

**You also need, per Click Me:**

| Item | Notes |
|---|---|
| One mechanical keyboard switch | Cherry MX compatible, 5-pin or 3-pin. This is the part that sets how hard the button is to press (see "Choosing your keyboard switch" in [ASSEMBLY.md](ASSEMBLY.md)) |
| A 3.5 mm mono cable | To connect the Click Me to the device it operates |
| Filament | For the four housing parts and one keycap |

No screws and no glue: the housing is snap-fit.

## 8. What it costs

These are the real figures from my own orders, in US dollars. **Treat them as a
ceiling, not a target**, for the reason given at the end of this section.

### The board order

25 assembled boards, ordered July 2026, shipped to the United States.

PCB manufacturing:

| Line | Cost |
|---|---|
| Engineering fee | $4.00 |
| Surface finish | $1.60 |
| Board | $11.80 |
| **Subtotal** | **$17.40** |

Assembly:

| Line | Cost |
|---|---|
| Setup fee | $25.56 |
| Stencil | $8.25 |
| Components | $2.08 |
| Extended components fee | $3.06 |
| SMT assembly | $0.20 |
| Packaging fee | $0.49 |
| **Subtotal** | **$39.64** |

What I actually paid:

| Line | Cost |
|---|---|
| Merchandise total | $57.00 |
| Shipping | $43.49 |
| Customs duties and taxes | $19.95 |
| Coupon discount | -$10.00 |
| PayPal fee | $0.55 |
| Sales tax | $9.60 |
| **Order total** | **$120.59** |
| **Per assembled board** | **$4.82** |

Two of those lines are mine rather than yours. The $10.00 was a coupon I happened
to have, and the PayPal fee depends on how you pay. Without the coupon the same
order is $130.59, or **$5.22 per board**, which is the safer number to budget
against.

### Everything else, per Click Me

| Item | Bought as | Per unit |
|---|---|---|
| Mechanical keyboard switch | $13.99 for 72 | $0.19 |
| PLA filament, 34.03 g | $12.47 per 1 kg roll | $0.42 |
| 3.5 mm mono cable | single | $3.00 |

Sources for the two Amazon items are in
[BOM.csv](BOM.csv).

### Cost of one finished Click Me

| Part | Cost |
|---|---|
| Assembled board | $4.82 |
| Mechanical keyboard switch | $0.19 |
| Printed housing and keycap | $0.42 |
| 3.5 mm mono cable | $3.00 |
| **Total** | **$8.43** |

Without the coupon, $8.83.

### How many to order

Most of what you pay is charged once per order rather than per board. The
engineering fee, the assembly setup fee and the stencil come to $37.81 before a
single board is made, and shipping, customs and tax added another $73.59, which is
61 percent of the total. Only about $16 of that $57 merchandise total actually
scaled with how many boards I asked for.

My own two orders show what that does to the per-board price:

| Order | Boards | Order total | Per board |
|---|---|---|---|
| Earlier revision | 50 | $118.10 | $2.36 |
| Current revision, in the photographs | 25 | $120.59 | $4.82 |

Twice as many boards for slightly less money. The arithmetic says order as many
as you will ever want in one go.

**Do not let it talk you into a big batch of an unproven board.** The 25-board
order is the smaller of the two on purpose. I had corrected something in the
design after the 50-board run, and I wanted boards in my hand to test before
committing to another large order. That is the right instinct, and the cost
structure makes it cheap advice to follow: because the per-order fees dominate,
a small proving batch costs almost the same as a large one, so you lose very
little by ordering 25 first and a great deal by ordering 100 of something with a
mistake in it.

So: order a small batch of any revision you have not held yet, confirm a
keyboard switch seats and the housing closes around it, and only then order the
quantity your lending library, school or caseload actually needs.

### These prices are higher than they need to be

Everything above was bought in small volumes, which is the worst case for price.
Every line in the bill of materials has room to come down with a bulk order.
The cable is the obvious target: at $3.00 it is the second most expensive part of
the whole device, and it is an ordinary audio cable. I will look at bulk pricing properly
once the design is finalised. Until then, budget from these numbers and expect to
beat them.

## 9. If something goes wrong

| What you see | What it usually means | What to do |
|---|---|---|
| Preview is blank or the wrong shape | The `.zip` was unzipped, or the wrong file was uploaded | Upload `Gerber_PCB1_2026-09-21.zip` exactly as downloaded |
| Board size is not about 46 x 46 mm | Wrong file, or units misread | Re-download and re-upload |
| A third part appears in the parts list | The files came from somewhere other than this repository | Re-download `BOM_ClickMe.csv` and `CPL_ClickMe.csv` |
| A part is out of stock | Normal | Accept a substitute in the same footprint, after reading its dimensions |
| JLCPCB emails an engineering question | Normal for a first order | Answer it; the order is paused until you do |
