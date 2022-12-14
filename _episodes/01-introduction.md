---
# Please do not edit this file directly; it is auto generated.
# Instead, please edit 01-introduction.md in _episodes_rmd/

title: "Nanopore-based sequencing: introduction"
teaching: 20
exercises: 0
questions:
- "What is nanopore-based sequencing?"
objectives:
- "Understand details of ONT sequencing platforms."
keypoints:
- "ONT produce a range of popular sequencing platforms."
- "This technology is constantly advancing."
source: Rmd

---




### What is this module about?

 - Long-read sequencing with the Oxford Nanopore Technologies (ONT) platform.
 - WHY?
    - recent technology advances have led to a surge in popularly for this platform.
    - Huge scope for really exciting (and low cost) science
    - Concepts and skills learned here are transferable to other sequencing technologies.
 - WHAT?
    - Genome assembly
    - RNA-seq
    - Variant identification (single base & structural)
    - Base modification (e.g., methylation)
    - Metagenomics


### ONT platforms


<img src="../fig/01-oxnano_2022.png" alt="plot of chunk unnamed-chunk-2" width="80%" style="display: block; margin: auto auto auto 0;" />

### The MinION

[http://www.nature.com/news/data-from-pocket-sized-genome-sequencer-unveiled-1.14724](http://www.nature.com/news/data-from-pocket-sized-genome-sequencer-unveiled-1.14724)

 - It's a USB stick sequencer!!
 - Rough specs (2014)
   - 6-8 hour run time
   - sequence per run: ~110Mbp
   - average read length: 5,400bp
   - reads up to 10kbp
   
 - 2022 specs: 
   - can run for up to 72 hours
   - Max yield per run: 50Gbp
   - Max read length recorded: >4Mbp

<img src="../fig/01-minion.png" alt="plot of chunk unnamed-chunk-3" width="50%" style="display: block; margin: auto auto auto 0;" />

<img src="../fig/01-nanopore-animation.gif" alt="plot of chunk unnamed-chunk-4" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com](https://nanoporetech.com)
[https://nanoporetech.com/products/specifications](https://nanoporetech.com/products/specifications)


### The MinION Mk1B

 - The MinION Mk1B is the current version of ONT's original sequencer.
 - Connects to a computer via USB.

<img src="../fig/01-minion-usb.png" alt="plot of chunk unnamed-chunk-5" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/products/minion](https://nanoporetech.com/products/minion)


<BR><BR><BR><BR>


<img src="../fig/01-minion-mk1b.png" alt="plot of chunk unnamed-chunk-6" width="50%" style="display: block; margin: auto auto auto 0;" />

### The MinION Mk1C

 - The MinION Mk1C provides a truly portable sequencing option, with built in compute and touchscreen.
 - For the price, however, the hardware is not particularly impressive.

<BR><BR><BR>
<img src="../fig/01-minion-mk1c.png" alt="plot of chunk unnamed-chunk-7" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/products/minion](https://nanoporetech.com/products/minion)


<img src="../fig/01-mk1c-spec-top.png" alt="plot of chunk unnamed-chunk-8" width="50%" style="display: block; margin: auto auto auto 0;" />

### The GridION

 - The GridION offers a "medium-throughput" option for Nanopore-based sequencing: 
 can run up to five flowcells at once.
 - The MinION (Mk1B and Mk1C) and GridION use the same flow cells
 - The Otago Genomics Facility has one of these.



<img src="../fig/01-gridion.png" alt="plot of chunk unnamed-chunk-9" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/products/gridion](https://nanoporetech.com/products/gridion)



### The Flongle

 - The Flongle uses an adapter to allow a smaller (and cheaper) flow cell to be used in the MinION and GridION devices.
 - Single-use system provides low-cost option for targeted sequencing (e.g., diagnostic applications).

<img src="../fig/01-flongle.png" alt="plot of chunk unnamed-chunk-10" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/products/flongle](https://nanoporetech.com/products/flongle)



### PromethION

 - The higher throughout PromethION uses a smaller cartridge-like flow cell. Two options: 24 or 48 flow cells.





<img src="../fig/01-promethion48.jpg" alt="plot of chunk unnamed-chunk-11" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/products/promethion](https://nanoporetech.com/products/promethion)

<BR>


<img src="../fig/01-promethion-flowcell.jpg" alt="plot of chunk unnamed-chunk-12" width="50%" style="display: block; margin: auto auto auto 0;" />



### Coming ~~soon~~ now: the P2



<img src="../fig/01-p2.png" alt="plot of chunk unnamed-chunk-13" width="70%" style="display: block; margin: auto auto auto 0;" />


Smaller device (standalone or connect to host computer) that can run Promethion flow cells.

[https://nanoporetech.com/products/p2](https://nanoporetech.com/products/p2)




### MinION flowcell characteristics

 - MinION flowcells typically have ~1200-1800 active pores (ONT guarantees at least 800 active pores).
 - Sequencing occurs at roughly 450 bases per second (ONT recommends keeping speed above 300 bases per second - additional reagents can be added to "refuel" the flowcell*)
 - BUT: pores are not constantly active, and can become blocked during the run 
 
 * [https://community.nanoporetech.com/protocols/experiment-companion-minknow/v/mke_1013_v1_revbm_11apr2016/refuelling-your-flow-cell](https://community.nanoporetech.com/protocols/experiment-companion-minknow/v/mke_1013_v1_revbm_11apr2016/refuelling-your-flow-cell)



### Nanopore technology



<img src="../fig/01-nanopore.png" alt="plot of chunk unnamed-chunk-14" width="70%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/how-it-works](https://nanoporetech.com/how-it-works)



### Nanopore technology

 - A motor protein (green) passes a strand of DNA through a nanopore (blue). The current is changed as the bases G, A, T and C pass through the pore in different combinations.

<img src="../fig/01-sequencing-animated_0.gif" alt="plot of chunk unnamed-chunk-15" width="60%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/how-it-works](https://nanoporetech.com/how-it-works)



### Nanopore movies

For more detailed information about ONT sequencing:

 - [https://nanoporetech.com/products/minion](https://nanoporetech.com/products/minion)
 - [https://nanoporetech.com/products/minion](https://nanoporetech.com/how-it-works)



### Technological advances...

 - Since its introduction, nanopore sequencing has seen a number of improvements.
 - The initial product was realtively slow, expensive (per base sequenced) and error prone (i.e., incorrect bases calls).
 - Incremental improvements have led to major advances in both speed and accuracy.

 
### 2D sequencing (prior to 2017)

 - Hairpin-based approach provided natural error detection methodology:
   - Link DNA strands with a hairpin adapter.
   - Sequence template strand followed by complement.
   - Basecall and compare sequences to produce consensus.



<img src="../fig/01-nanopore-2d-reads.png" alt="plot of chunk unnamed-chunk-16" width="50%" style="display: block; margin: auto auto auto 0;" />

Jain, et al. The Oxford Nanopore MinION: delivery of nanopore sequencing to the genomics community. Genome Biol 17, 239 (2016). 
[https://doi.org/10.1186/s13059-016-1103-0](https://doi.org/10.1186/s13059-016-1103-0)



### What happened to 2D reads?



<img src="../fig/01-2d-reads.png" alt="plot of chunk unnamed-chunk-17" width="50%" style="display: block; margin: auto;" />

[https://bioinformatics.stackexchange.com/questions/5525/what-are-2d-reads-in-the-oxford-minion/5528](https://bioinformatics.stackexchange.com/questions/5525/what-are-2d-reads-in-the-oxford-minion/5528)



### The hairpin lawsuit...

 - PacBio (competitor in the long-read space) and ONT have filed a number of lawsuits against each other over the past few years.


<img src="../fig/01-europe-lawsuit.png" alt="plot of chunk unnamed-chunk-18" width="50%" style="display: block; margin: auto;" />


[https://www.genomeweb.com/sequencing/pacbio-oxford-nanopore-settle-patent-dispute-europe](https://www.genomeweb.com/sequencing/pacbio-oxford-nanopore-settle-patent-dispute-europe)

 

### 1D$^2$ sequencing

 - In 2017 ONT announced the new 1D$^2$ chemistry
 - Showed higher accuracy that 1D (and SAID it was better than 2D)
 - It didn't last long... 



<img src="../fig/01-1D2-accuracy.png" alt="plot of chunk unnamed-chunk-19" width="50%" style="display: block; margin: auto auto auto 0;" />

 - Video at link below:

[https://nanoporetech.com/about-us/news/1d-squared-kit-available-store-boost-accuracy-simple-prep](https://nanoporetech.com/about-us/news/1d-squared-kit-available-store-boost-accuracy-simple-prep)



### Pore imporvements: the R10 pore

 - ONT introduced the new R10 pore in 2019 (previous was R9.4.1).
 - Main differences were *longer barrel* and *dual reader head:* gave improved resolution of homopolymer runs.




<img src="../fig/01-r10-pore.png" alt="plot of chunk unnamed-chunk-20" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/about-us/news/r103-newest-nanopore-high-accuracy-nanopore-sequencing-now-available-store](https://nanoporetech.com/about-us/news/r103-newest-nanopore-high-accuracy-nanopore-sequencing-now-available-store)



### R10.3 vs R9.4.1 performance 

 - With a bit more tweaking (to get to R10.3) ONT improved 1D (i.e., single-strand) sequencing accuracy, although throughput is still not as high as the R.9.4.1 pore.

<img src="../fig/01-r10.3-results.png" alt="plot of chunk unnamed-chunk-21" width="70%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/about-us/news/r103-newest-nanopore-high-accuracy-nanopore-sequencing-now-available-store](https://nanoporetech.com/about-us/news/r103-newest-nanopore-high-accuracy-nanopore-sequencing-now-available-store)



### Q20+: the return of 2D reads...

- The previous ONT products are "Q10" (we'll discuss this soon), meaning that the error rate is roughly 1 incorrect base call per 10 bases (that's high!)
- The new "Q20+" products are now available  - moves to less than 1 error per 100 bases (a little more respectable, but still well below short-read technologies like Illumina).
- Upgrade includes a return to the "2D" approach.


<img src="../fig/01-lawsuit2020.png" alt="plot of chunk unnamed-chunk-22" width="50%" style="display: block; margin: auto;" />

[https://www.genomeweb.com/sequencing/jury-invalidates-pacific-biosciences-patents-lawsuit-against-oxford-nanopore#.YOt8e26xXUI](https://www.genomeweb.com/sequencing/jury-invalidates-pacific-biosciences-patents-lawsuit-against-oxford-nanopore#.YOt8e26xXUI)



### Making improvements

<img src="../fig/01-ont-screening.png" alt="plot of chunk unnamed-chunk-23" width="80%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies](https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies)



### Q20+ and Kit 14

<img src="../fig/01-ont-q20.png" alt="plot of chunk unnamed-chunk-24" width="480" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/q20plus-chemistry](https://nanoporetech.com/q20plus-chemistry)



### Nanopore accuracy


<img src="../fig/01-ont-accuracy.png" alt="plot of chunk unnamed-chunk-25" width="50%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/accuracy](https://nanoporetech.com/q20plus-chemistry)



### Duplex (and simplex) accuracy


<img src="../fig/01-ont-duplex-q30.png" alt="plot of chunk unnamed-chunk-26" width="80%" style="display: block; margin: auto auto auto 0;" />

What aren't they telling us about those duplex reads...? 

[https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies](https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies)



### Coming... sometime - the Mk1D



<img src="../fig/01-ont-mk1d.png" alt="plot of chunk unnamed-chunk-27" width="70%" style="display: block; margin: auto auto auto 0;" />

[https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies](https://nanoporetech.com/resource-centre/london-calling-2022-update-oxford-nanopore-technologies)
[https://nanoporetech.com/products/minion-mk1d](https://nanoporetech.com/products/minion-mk1d)


### More Nanopore: London Calling 2022



<img src="../fig/01-lc22.png" alt="a figure caption" width="50%" style="display: block; margin: auto auto auto 0;" />

 - Online conference held in May 2022
 - Talk videos available online
 - LOTS of really cool announcements and research applications

[https://nanoporetech.com/lc22](https://nanoporetech.com/lc22)



