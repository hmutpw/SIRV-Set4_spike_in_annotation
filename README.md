# SIRV-Set4_spike_in_annotation

#### 1. ERCC.SIRV.longSIRV.genome.fa

The genomic sequences of SIRV-Set4 spike-in controls, download from https://www.lexogen.com/wp-content/uploads/2021/06/SIRV_Set4_Norm_Sequences_20210507.zip

#### 2. ERCC.SIRV.longSIRV.transcripts.with.polyA.tail.fa

This file is suggested for studies aimed at biological data analysis.
The transcript sequences of ERCC+SIRV+longSIRV spike-in transcripts, and polyA tail were included. The header information is as follows:
">transcript_id|gene_id|strand|transcript_length(include polyA)|tag|polyA_length"

For SIRVs, this file only includes transcripts tagged as 'positive', which means all the transcripts were included in the kit.

#### 3. ERCC.SIRV.longSIRV.annotation.gtf

This file is suggested for studies aimed at biological data analysis.

The exon annotation of ERCC+SIRV+longSIRV spike-in transcripts.

Here, we made a few modifications to SIRV spike-in transcripts, we labeled 'A', 'B', 'C', and 'D' after the gene IDs based on the structure of these transcripts from the same genomic region. Transcripts with the same gene ID indicate they are different isoforms from the same gene locus, while transcripts with different postfixes (e.g., SIRV3A, SIRV3B) indicate they should be different genes since they are from two different strands.

This kind of modification came from the LRGASP project (https://lrgasp.github.io/lrgasp-submissions/docs/reference-genomes.html), but I made a small change. Because SIRV406 overlaps with SIRV401/2/7 but does not overlap with SIRV403/4/5/8. In LRGASP annotation, SIRV406 is from SIRV4B (a single-isoform gene). But here we believe SIRV406 belongs to SIRV1A because it partially overlaps with SIRV401/2/7. So we do not have SIRV4B in our annotation files to distinguish with LRGASP annotation.

To avoid the longSIRV have the same transcript_id and gene_id, we add *-001 to the transcript ids. For example, transcript_id of SIRV4001 is SIRV4001-001. (2024-11-20)

To generate a complete annotation, we add gene and transcript features in the `gtf` file, ensure the IsoQuant can generate a complete annotation.(2024-11-21)

#### 4. ERCC.SIRV.longSIRV.transcripts.extended.with.polyA.tail.fa

This file is suggested for studies aimed at tool development.
The header format is the same with 'ERCC.SIRV.longSIRV.transcripts.with.polyA.tail.fa', but we added the annotation of 'negative' tagged transcripts even if these RNA molecules were not included in the kits.
For SIRVs, this file includes transcripts tagged as both 'positive' and 'negative', while 'negative' can be used as negative controls when evaluating tools' performance.

#### 5. ERCC.SIRV.longSIRV.extended.annotation.gtf

This file is suggested for studies aimed at tool development.

The format is the same with 'ERCC.SIRV.longSIRV.annotation.gtf', but we added the annotation of 'negative' tagged transcripts even if these RNA molecules were not included in the kits.

For SIRVs, this file includes transcripts tagged as both 'positive' and 'negative', while 'negative' can used as negative controls when evaluating the performance of tools.

To avoid the longSIRV have the same transcript_id and gene_id, we add *-001 to the transcript ids. For example, transcript_id of SIRV4001 is SIRV4001-001. (2024-11-20)

To generate a complete annotation, we add gene and transcript features in the `gtf` file, ensure the IsoQuant can generate a complete annotation.(2024-11-21)

#### 6. SIRV_Set4_transcript_annotation.txt/SIRV_Set4_transcript_annotation.xlsx

This file includes the information extracted from SIRV-Set4 sequence design information files (https://www.lexogen.com/wp-content/uploads/2021/06/SIRV_Set4_Norm_sequence-design-overview_20210507a.xlsx).

#### 7. SIRV_Set4_Norm_sequence-design-overview_20210507a.xlsx

download from https://www.lexogen.com/wp-content/uploads/2021/06/SIRV_Set4_Norm_sequence-design-overview_20210507a.xlsx.

Please feel free to contact me is you have any question.
