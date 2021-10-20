# Leismore Shorter ID Specification v1.0.0

## Introduction

Leismore Shorter ID is a universally unique identifier based on [Nano ID](https://github.com/ai/nanoid) (Sitnik [2017] 2021). This document describes its purpose, format, recommended comparison method, and other technical details.

## Differences from Leismore Short ID

The Short ID is designed for digital medias, while the Shorter ID is for non-digital medias such as paper and with more considerations for human readability or sharing requirement.

Comparison the Short ID, Leismore Shorter ID is:

1. Shorter
2. Case-insensitive
3. Increased collision chance

## Purpose and Designing Considerations

Ideally, a universally unique identifier exposing to end-users or external applications via non-digital medias, should be:

1. No collision in the near future
2. Friendly for human readers
3. URL friendly character set
4. Short and fixed length
5. Case-insensitive

## Format

* Character set ( inspired by `nolookalikes` from [Nanoid-Dictionary](https://github.com/CyberAP/nanoid-dictionary) (Lashmanov [2018] 2021) ):
  -                    `346789ABCDEFGHJKMNPQRTWXY`
* Length:              16 characters
* Canonical syntax:    XXXX-XXXX-XXXX-XXXX (Uppercase)
* Case-insensitive

## Recommended Comparison Method

The `-` characters are used purely for the human readability reason. It must not be considered as a semantics part in Leismore Shorter ID. While doing ID comparison, it must be removed from the IDs.

## Chance of Collision

When 1,000 IDs are being generated per hour, in order to have a 1% probability of at least one collision, **~2 thousand years** are needed, according to the calculation of [Nano ID CC](https://zelark.github.io/nano-id-cc) (Zhuravlёv n.d.)

## References

* Sitnik, Andrey. (2017) 2021. Nano ID. JavaScript. https://github.com/ai/nanoid.
* Lashmanov, Stanislav. (2018) 2021. Nanoid-Dictionary. JavaScript. https://github.com/CyberAP/nanoid-dictionary.
* Zhuravlёv, Aleksandr. n.d. Nano ID CC. Web. Accessed October 19, 2021. https://zelark.github.io/nano-id-cc.
