# Gene Fusion Lab (BIS 101)

This is a single-page exercise for designing a DNA junction between two short model genes. Students aim to produce one continuous open reading frame (ORF) that retains the **SYG** motif in toy-GFP and the **HGG** motif in Partner. Toy-GFP is a teaching sequence, not a fluorescent protein.

## Open the lab

Open `index.html` in a modern web browser. The page runs locally; no installation, server, or internet connection is needed. Refresh the browser after editing the file.

## Student workflow

1. **Choose the protein order.** `Toy-GFP → Partner` puts toy-GFP at the N terminus. `Partner → Toy-GFP` puts it at the C terminus.
2. **Choose both gene cuts.** The first slider sets the last base kept from the first gene. The second slider sets the first base kept from the second gene. The `−` and `+` buttons move a cut one base at a time. Displayed base numbers include the six-base flanks. Square brackets mark each coding sequence; the orange bar marks the cut. Gold marks the motifs to preserve. The first gene's 3′ flank is rejected. The second gene's 5′ UTR can be included if the fusion passes the frame and stop checks; any amino acids it adds are flagged for review.
3. **Optionally add a linker.** Check **Add a linker**, then generate random DNA or enter your own A/C/G/T sequence of up to 15 bases. Random generation offers lengths from 3 to 15 bases in steps of three; entered DNA may be any length from 1 to 15 bases. Spaces in entered DNA are ignored. The two linker sliders select the first and last *bases* to include. Purple bases are included; gray bases are omitted. The linker is shown as DNA, since its reading frame depends on the preceding gene cut.
4. **Inspect stop markers.** Red markers below the linker sequence show stop triplets in the assembled fusion's reading frame that overlap selected linker bases. A stop may span a gene–linker junction. The markers update when gene cuts or linker selections change. They do not mark unused linker bases.
5. **Select Check fusion.** The page opens the **reading frame from the first gene's ATG** beneath the DNA junction preview. Each box shows an assembled DNA codon and its amino acid. Orange lines mark joins; gold boxes contain 5′ UTR bases; red boxes identify premature stops; and faded boxes are downstream of the first stop. The result also shows the translated product through that stop, explains any problems, and lists amino acids added from the second gene's 5′ UTR for review. **Show a hint** suggests a starting strategy. **Reset cuts** resets the gene cuts for the selected protein order; it does not remove or regenerate the linker.

## How a fusion passes

The first gene must supply the initial `ATG`, and the second gene must supply the final in-frame stop. The first gene's 3′ flank is excluded. The second gene's 5′ UTR is permitted, but any added amino acids should be reviewed. Both motifs must remain in the translated product. The assembled DNA must place the second gene back in its original reading frame and contain no earlier in-frame stop. A linker can complete a partial codon at a junction; its length alone does not determine whether the fusion is in frame.

For a first attempt, cut just before the first gene's stop codon and just after the second gene's `ATG`. Check the result, then move a gene cut by one base and test whether a linker base can restore the second gene's frame.

## Scope

The sequences and motif labels are simplified for instruction. A passing result means the page's sequence and frame checks passed. It does not establish that a real fusion protein would fold, localize, fluoresce, or function. The exercise does not model cloning chemistry, regulatory DNA, splicing, or expression levels.
