[[2022-11-29]], [[2022-12-01]]

1. Gel Electrophoresis
	- Separates [[DNA]] fragments by size
	- You put a piece of DNA under an electric current
		1. [[DNA]] is negatively charged
		2. If you put it under electric current, it migrates towards positive pole
	- Gel is made of agarose and polyacrylamide
		1. Carbohydrates
		2. Get better resolution w/ acrylamide but agar can give you approximation of DNA size
	- Submersed in buffer that can carry current and subjected to an electrical field
	- Larger fragments move slower while smaller fragments move faster
		1. Like a race where fastest (smallest) pieces are in front and slower are behind
		2. Pieces that move fastest and farthest are smallest and vice versa
	- [[DNA]] is visualized using fluorescent dyes
		1. The dye binds to DNA ([[DNA]] has major and minor grooves)
			- Typically binds in minor groove
		2. Called EtBr (ethidimine bromide)
		3. The brightest pieces has the most mass (more DNA)
	- Have a molecular ladder on the side for comparison
		1. It has pieces of DNA with known sizes and increments 
		2. If it is 100 base pair ladder, smallest is 100 then 2nd is 200 then 3rd is 300 and so on
2. Polymerase chain reaction (PCR)
	- Developed by Kary Mullis, who was awarded a nobel prize for this technique
	- Allows the amplification of a small [[DNA]] fragment using primers that flank the region
		1. Critical enzyme for [[DNA Replication]] is DNA polymerase
			- Nucleotides are building blocks
			- DNA pol must have primer to function
		2. Must be done in buffer environment w/ ideal temp and pH
		3. If you have a piece of [[DNA]] that you want to copy, and its complimentary to primer, you can replicate outside the [[Cell]]
		4. Mullis did this w/ E coli polymerase
			- E coli ideal temp is our body temp (about 37 * C)
			- Took double stranded DNA and heated it up (which denatures it (H bonds come apart)) then cools it to allow primer to bind. Once primer is bound, [[DNA]] pol can work.
	- Each PCR cycle involves three steps
		1. Denaturation (high temp - about 95 * C)
		2. Annealing of primers (low temp)
		3. DNA synthesis (intermediate temp)
			- Taq polymerase
	- Had to add more polymerase every time cycle is repeated and DNA is rereplicated
		1. Denaturation process also damages polymerase
		2. Mullis then noticed heat resistant bacteria from hot springs
			- Their DNA pol can handle the heat
			- This is taq polymerase (doesn't denature during temporary denature process)
	- Copied [[DNA]] in a test tube instead of a [[Cell]]
		1. Bc it was a smaller piece, it could be done more quickly than normal E coli
			- Faster than 20 minute binary fission process
	- Applications of PCR
		1. Allows the investigation of minute samples of DNA
		2. Many many applications
		3. Forensics, 23 in me, etc.
			- All can amplify [[DNA]] and look for specific regions
		4. Can take one copy and do twenty cycles (resulting in a mil copies)
			- Can be done in two hours
		5. Detection of genetic defects in embryos by analyzing a single [[Cell]]
		6. Analysis of mitochondrial DNA
	- PRC critical components
		1. Primers = short pieces of DNA complementary to each end of the target sequence
		2. Taq polymerase = a [[DNA]] polymerase isolated from the thermostable bacterium *Thermus aquaticus*
		3. dNTPs = deoxyribonucleotide triphosphates
		4. Rx buffer = ---
		5. ---
	- Southern blotting is used to find a particular sequence in a sample of DNA
		1. DNA fragments are separated on a gel, transferred to a nylon membrane, and incubated w/ a [[DNA]] probe complementary to the sequence of interest
			- DNA probe is single stranded
				1. Longer than a primer but still pretty short
				2. While primer may be 10-20, a probe may be 100-200
			- If it is complementary, the two DNA fragments anneal
				1. Anneal = the coming together of complementary strands
				2. Annealing temp is required for binding
		1. Northern blotting is similar to Southern blotting, but RNA is run on the gel instead of DNA
		2. In Western blotting, proteins are run on a gel and detected using antibodies
		3. ---
3. Molecular Cloning
	- Clone = genetically identical copy
	- Molecular cloning = isolation of a specific [[DNA]] sequence (usually [[Protein]]-encoding)
		1. Sometimes called gene cloning
	- The most flexible and common host for cloning is E coli
	- Gfp lab was based upon molecular cloning
		1. Typically use a plasmid (bacterial chromosomes (small and circular))
			- Ideal for taking a plasmid, opening the circle, and inserting a piece of foreign DNA into the circle
			- 3 components of plasmids
				1. Origin of replication (allows independent replication)
				2. Selectable marker (allows presence of plasmid to be easily identified)
				3. Multiple cloning site (MCS)
		2. We took gfp gene from jellyfish and inserted it in an E coli plasmid
			- gfp gene is a selectable marker
			- amp gene also a selectable marker in the lab
			- Vector = plasmid that will carry foreign DNA
	- Yeast is eukaryote
		1. Has one of smallest genome of eukaryotes
		2. Yeast artificial chromosomes can be utilized for inserting pieces of DNA 
		3. Large pieces of DNA (10s of thousands of bases) can use YAKs and VAKs whereas small pieces use vectors
	- You have a plasmid w/ a restriction site in middle of a gene (lac z in the graphic, which is used in lac operon for lactose (operon = one RNA that codes for multiple proteins))
		1. If you suddenly put bunch of DNA in lac operon, it will completely change lac Z gene
		2. We can take DNA and have cloning site in middle of lac operon and lac Z gene
			- Restriction endonuclease = specifically targets precise sequence of DNA
				1. Foreign DNA and plasmid are cut w/ the same restriction endonuclease enzyme that can recognize restriction site
				2. The restriction enzyme creates sticky ends, which allow the foreign DNA and cloning vector to anneal
					- Sticky ends are complementary and naturally want to anneal
					- Foreign DNA and plasmid have exact same recognition site
				3. An enzyme called ligase glues the annealed fragments together
				4. The ligated cloning vector is transformed into a bacterial host strain that is ampicillin sensitive and is missing the lac Z gene from its genome
				5. Bacteria are then grown on media containing ampicillin and X-gal, a chemical that is metabolized by same pathway as lactose
				6. The ampicillin kills bacteria without plasmid
					- Selectable marker can be ampicillin resistance
				7. If lac Z gene is intact (no insert), in presence of modified sugar called X-gal, the colonies will be blue
					- Undisrupted genes are blue
					- Blue colonies have plasmids without insert
				8. If modified, the colonies have plasmids w/ foreign insert
				9. ---
	- DNA libraries
		1. A collection of DNAs in a vector that taken together represent the complex mixture of DNA
		2. Some endonucleases will cut through both strands (leaving blunt ends instead of overhanging sticky end)
			-  Different endonucleases can also recognize different lengths of bases
				1. Ex: 4 cutter can recognize G A T C while 6 cutter can recognize A T G G C C
					- 4 cutter is more likely to recognize more strands
			- Endonucleases come from defense systems of bacteria
				1. Bacteria may be exposed to bacteriophages (viruses that attack bacteria)
				2. Endonucleases recognize virus and cut it up
				3. Some in eukaryotes, but prokaryotes are common source
			- We can collect pieces of DNAs and store it in libraries
				1. Use endonucleases to cut up DNA
					- We have telomeric DNA, centromeric DNA, non coding (introns) and coding regions (exons)
						- Contains inactive regions and active regions
						- Less specific than cDNA
					- Genomic library represents the entire genome in a vector
		3. Genome is randomly fragmented in genomic library and inserted in a vector
			- Introduced in host cells
			- Usually constructed in BACs
		4. Complementary DNA (cDNA)
			- Very specific information about what protein an RNA can make
			- mRNA isolated
				1. Represents only actively used genes
				2. No introns
			- We use *reverse transcriptase* to make cDNA
				1. Reverse transcriptase can take RNA and turn it back into DNA
					- DNA lasts much longer than RNA
				2. cDNA used to make library
					- Stored information about RNA and proteins
				3. All genomic libraries from a cell will be the same but cDNA libraries can be different
			- Nothing but code info (no introns)
		5. DNA fragments from source DNA using endonucleases
			- Fragments can be individual expressed RNA
			- DNA then inserted into plasmid vector (transformation occurs)
			- Each cell then contains a single fragment and all cells together are the library
		6. How does reverse transcriptase work? - Production of cDNA
			- Take Eukaryotic DNA template
			- Transcription
			- Primary RNA transcript
			- Introns are cut out and coding regions are spliced together
			- Mature RNA transcript
			- Isolation of mRNA and addition of reverse transcriptase
			- Reverse transcriptase utilizes mRNA to create cDNA
			- Addition of mRNA degrading enzymes lead to degraded mRNA so you just end up with cDNA
			- DNA polymerase turns single stranded cDNA into double stranded cDNA w/ no introns
4. Reproductive Cloning
	- Dolly the sheep was first mammal to be cloned
		- To create Dolly, the nucleus was removed from donor egg cell
		- The nucleus from a second sheep (from mammary cells) was then introduced into the enucleated cell and combined using direct current pulse
		- Then allowed to divide to the blastocyst stage before being implanted into surrogate mother
		- Dolly showed characteristics of older ewe
			1. Older DNA/cells
5. [[Biotechnology in Medicine and Agriculture]]
6. Genomics and other "omics"
	- Genomics = study of entire genomics at level of DNA
	- Proteomics = study of entire set of proteins
	- Transcriptomics = study of entire set of mRNAs expressed in an organism
	- Transcriptomics = study of entire set of mRNAs expressed in an organism
	- Mitochondrial Genomics = maternally inherited to next generation
	- Metagenomics = study of collective genomes within an environmental sample
		1. Involves isolating DNA from multiple species within an environmental niche
		2. You could take samples of water from different areas
			 - Differences between environments
			 - --- (graphic)
	- Pharmacogenomics (aka toxicogenomics) = study of transcription profiles of genes in response to the presence of a chemical/drug