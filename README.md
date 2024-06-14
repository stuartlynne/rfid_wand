# [Low Cost RFID Wand](https://github.com/stuartlynne/rfid_wand)
# Thu Jun 13 01:55:25 PM PDT 2024

This describes how to build low-cost RFID Wands for to read and write UHF RFID tags.

Using these with (for example) and Impinj R420 reader, you can read and write UHF RFID tags from four stations at once.

The original use of these was with [RaceDB](https://github.com/esitarski/RaceDB) to read and write tags for cycling races.

*The estimated cost of the wand is about USD 25.*

This contrasts with the cost of commercial Near Field RFID antennas which can be USD 200-350 each.

E.g. [Impinj Mini-Guardrail] (https://www.atlasrfidstore.com/impinj-mini-guardrail-ilt-lp-indoor-rfid-antenna-global/)


## Parts

<img src=./imgs/parts-overview.jpg width=200 height=200>

- 5dBi PCB UHF RFID 902-928M Antenna 5cm*5cm with SMA
- 3m cable with RP-TNC Male and SMA
- paint scraper
- double sided mounting tape
- plastic tape
- 40mm shrink wrap


## Tools
- heat gun

## Assembly

1. Mount the antenna on the paint scraper using the double-sided tape
2. Attach long cable to the antenna pigtail
3. Gently wrap around the paint scraper and secure it with plastic tape
4. Test the antenna with the RFID reader to ensure it is working (e.g. RaceDB)


| Step 1 | Step 3 |
| -- | -- |
|<img src=./imgs/mount1.jpg width=200 height=200>|<img src=./imgs/mount2.jpg width=200 height=200>|


5. Cut the shrink wrap to length and insert assembly into the shrink wrap
6. Heat the shrink wrap with the heat gun to secure the assembly

| Step 5 | Step 6 |
| -- | -- |
|<img src=./imgs/shrink1.jpg width=200 height=200>|<img src=./imgs/shrink2.jpg width=200 height=200>|



## RFID Reader Configuration

If used with the default power configuration the RFID wand will be too powerful and will read tags from too far away.
It may also be able to accidentally write tags that are not intended to be written.

If using RaceDB these are the settings that should be used:

```
# This will configure the Impinj reader for reading/writing RFID tags. 
#   - set power and sensitivity for Impinj R1000 using Lilly 5dBi PCB UHF RFID Patch antenna wands
#
export RFID_TRANSMIT_POWER=40
export RFID_RECEIVER_SENSITIVITY=20
```

## Usage

The power settings assume a metal paint scraper is used to limit the directionality of the antenna.  

Scanning with the want should be done with the tag on the antenna side.

## Packaging

| | |
| -- | -- |
| <img src=./imgs/case1.jpg width=200 height=200>|<img src=./imgs/case2.jpg width=200 height=200>|
| <img src=./imgs/use1.jpg  width=200 height=200> |


## 5dBi PCB UHF RFID 902-928M Antenna 5cm*5cm with SMA 

Example source: [AliExpress](https://www.aliexpress.com/item/4001021595653.html)

The cost of the antenna is about USD 5.00 plus shipping. If you are buying at least ten, various vendors will
offer to customize them with the extension cable and connector of your choice for a lower overall cost.

## RFID Cable

See the note above in the Antenna section. 

For limited quantities, the cost of the cable is about USD 20.00, depending on your source.

Locally we used MRO Electronics which had a good selection of cables and connectors and could make custom cables. The cost for a half
dozen 3m cables with RP-TNC Male connector and SMA connector was about $20.00 Cdn each.

## RFID Reader

We use Impinj R1000 and R420 readers.  These are available on eBay for about $200-$600 USD.

The R1000 readers are (almost) indestructible and we have some that have been in use for over 10 years.


## Links

[Connector Types from Impinj](https://support.impinj.com/hc/en-us/articles/202756398-RF-Connector-Types)

## [Related Projects](related.md)




