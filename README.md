# Low Cost RFID Wand
# Thu Jun 13 01:55:25 PM PDT 2024

This describes how to build low cost RFID Wands for to read and write UHF RFID tags.

Using these with (for example) and Impinj R420 reader, you can read and write UHF RFID tags from four stations at once.

The original use of these was with [RaceDB](https://github.com/esitarski/RaceDB) to read and write tags for cycling races.

*The estimated cost of the wand is about $25.00 USD.*

This contrasts with the cost of commercial Near Field RFID antennas which can be $200-$350 USD each.

E.g. [Impinj Mini-Guardrail] (https://www.atlasrfidstore.com/impinj-mini-guardrail-ilt-lp-indoor-rfid-antenna-global/)


## Parts

| Part Overview |
|![Parts Overview](images/parts-overview.jpg)|

- 5dBi PCB UHF RFID 902-928M Antenna 5cm*5cm with SMA
- 3m cable with RP-TNC Male and SMA
- paint scraper
- double sided mounting tape
- plastic tape
- 40mm shrink wrap


## Tools
- heat gun

## Assembly

1. Mount the antenna on the paint scraper using the double sided tape
2. Attach long cable to the antenna pigtail
3. Gently wrap around the paint scraper and secure with plastic tape
4. Test the antenna with the RFID reader to ensure it is working (e.g. RaceDB)


| Step 1 | Step 3 |
|![Step 1](images/mount1.jpg)|![Step 2](images/mount2.jpg)|

5. Cut the shrink wrap to length and insert assembly into the shrink wrap
6. Heat the shrink wrap with the heat gun to secure the assembly

| Step 5 | Step 6 |
|![Step 3](images/shrink1.jpg)|![Step 4](images/shrink2.jpg)|


## RFID Reader Configuration

If used with the default power configuration the RFID wand will be too powerful, and will read tags from too far away.
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

The power settings assume a metal paint scraper is used to limit directionality of the antenna.  

Scanning with the want should be done with the tag on the antenna side.

## Packaging

| -- | -- |
|![Packaging](images/case1.jpg)|
|![Packaging](images/case2.jpg)|
|![In use](images/use1.jpg)|


## 5dBi PCB UHF RFID 902-928M Antenna 5cm*5cm with SMA 

Example source: [AliExpress](https://www.aliexpress.com/item/4001021595653.html)

Cost of the antenna is about $5.00 USD plus shipping. If you are buying at least ten, various vendors will
offer to customize them with the extension cable and connector of your choice for a lower overall cost.

## RFID Cable

![RP-TNC Male](images/cable.jpg)

See note above. 

For limited quantities, the cost of the cable is about $20.00 USD, depending on your source.

Locally we used MRO Electronics who had a good selection of cables and connectors and could make custom cables. Cost for a half
dozen 3m cables with RP-TNC Male connector and SMA connector was about $20.00 Cdn each.

## RFID Reader

We use Impinj R1000 and R420 readers.  These are available on eBay for about $200-$600 USD.

The R1000 readers are (almost) indestructible and we have some that have been in use for over 10 years.


## Links

| Description | Link |
|Connector Types from Impinj|[https://support.impinj.com/hc/en-us/articles/202756398-RF-Connector-Types](https://support.impinj.com/hc/en-us/articles/202756398-RF-Connector-Types)|

## [Related Projects](related.md)




