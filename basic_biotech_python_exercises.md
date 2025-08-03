## 1. GC Count Check

**Question:** Given a DNA string `seq = "ATGCGCTAAG"`, count G and C and print “High GC” if ≥ 5, else “Low GC.”

```python
seq = "ATGCGCTAAG"
if seq.count('G') + seq.count('C') >= 5:
    print('High GC')
else:
    print('Low GC')
```

**Concept:** Uses string methods and arithmetic to quantify nucleotide composition and apply a conditional threshold.\
**Real-life Use:** Screening oligonucleotides for GC content helps predict melting temperatures before primer design.

---

## 2. Purine vs Pyrimidine

**Question:** For a nucleotide `nt = "A"`, print “Purine” if it’s A or G, else “Pyrimidine.”

```python
nt = "A"
if nt in ('A', 'G'):
    print('Purine')
else:
    print('Pyrimidine')
```

**Concept:** Demonstrates membership testing in tuples and simple branching logic for classification.\
**Real-life Use:** Classifying bases informs enzymatic cleavage patterns or mismatch modeling in sequencing.

---

## 3. Sequence Length Validation

**Question:** Given `seq`, check if `len(seq) % 3 == 0`; print “Valid ORF” or “Invalid ORF.”

```python
seq = "ATGCGT"
if len(seq) % 3 == 0:
    print('Valid ORF')
else:
    print('Invalid ORF')
```

**Concept:** Uses `len()` and modulo operator to enforce biological constraint of codon triplets.\
**Real-life Use:** Verifying open reading frames ensures gene fragments will translate correctly without frameshifts.

---

## 4. Complement at Position

**Question:** Given `seq = "ATGC"` and `i = 2`, check if `seq[i]` complements a provided `base = "A"`.

```python
seq = "ATGC"
i = 2
base = 'A'
complements = {'A':'T', 'T':'A', 'G':'C', 'C':'G'}
if complements.get(seq[i]) == base:
    print('Complementary')
else:
    print('Not complementary')
```

**Concept:** Maps bases via a dictionary and uses indexing to verify complementarity.\
**Real-life Use:** Ensuring probe or primer bases pair correctly to target sequences in hybridization assays.

---

## 5. Primer End Check

**Question:** Given a primer string, check if it ends with "GC".

```python
primer = "ATGCGC"
if primer.endswith('GC'):
    print('Has GC clamp')
else:
    print('No GC clamp')
```

**Concept:** Leverages string slicing method `endswith()` to detect a GC clamp important for primer stability.\
**Real-life Use:** GC clamps at the 3′ end raise primer melting temps, improving PCR specificity.

---

## 6. Convert Gene Names

**Question:** Uppercase `genes = ["tp53", "brca1", "egfr"]` and test if "TP53" is in list.

```python
genes = ["tp53", "brca1", "egfr"]
upper_genes = [genes[0].upper(), genes[1].upper(), genes[2].upper()]
if 'TP53' in upper_genes:
    print('TP53 found')
else:
    print('TP53 not found')
```

**Concept:** Uses list indexing and the `upper()` string method to normalize identifiers for robust comparison.\
**Real-life Use:** Standardizing gene symbols avoids mismatches when querying genomic databases.

---

## 7. Molecular Weight Lookup

**Question:** Given `mw = {"Ala":89, "Gly":75}`, retrieve weight of "Gly" and compare to 80.

```python
mw = {"Ala": 89, "Gly": 75}
if mw['Gly'] < 80:
    print('Light amino acid')
else:
    print('Heavy amino acid')
```

**Concept:** Demonstrates dictionary access and conditional comparison for biochemical properties.\
**Real-life Use:** Identifying light vs heavy residues aids in designing peptides for mass spectrometry.

---

## 8. Three-Sample Average Mass

**Question:** Compute average of `m1, m2, m3` and check if ≥ 100.

```python
m1, m2, m3 = 110.5, 95.0, 102.3
avg = (m1 + m2 + m3) / 3
if avg >= 100:
    print('Average mass >= 100')
else:
    print('Average mass < 100')
```

**Concept:** Uses arithmetic operators to calculate mean and a conditional to interpret results.\
**Real-life Use:** Averaging replicate measurements filters experimental noise in concentration assays.

---

## 9. Amino Acid Presence

**Question:** Check if "W" is in `protein = "MKTLLILAV"`.

```python
protein = "MKTLLILAV"
if 'W' in protein:
    print('Contains tryptophan')
else:
    print('No tryptophan')
```

**Concept:** Simple substring membership test to detect amino acid residues.\
**Real-life Use:** Detecting rare residues like W helps predict functional sites in proteins.

---

## 10. Codon Stop-Check

**Question:** Test if `codon = "UAA"` is in `{'UAA','UAG','UGA'}`.

```python
codon = 'UAA'
stop_codons = {'UAA', 'UAG', 'UGA'}
if codon in stop_codons:
    print('Stop codon')
else:
    print('Not a stop codon')
```

**Concept:** Uses set membership for efficient lookup of stop codons.\
**Real-life Use:** Identifying stop codons is vital when annotating gene translations.

---

\*(Exercises 11–50 follow the same pattern: solution, concept, and real-life biotechnology use case.

---

## 11. Unique Codons

**Question:** From `codons = ('AUG','UUU','AUG')`, count unique codons.

```python
codons = ('AUG', 'UUU', 'AUG')
unique = set(codons)
print(len(unique))  # prints 2
```

**Concept:** Converts tuple to set for deduplication and uses `len()`.\
**Real-life Use:** Evaluating codon usage diversity in small gene fragments.

---

## 12. Update Restriction Sites

**Question:** Append "GGATCC" to `sites = ["GAATTC","AAGCTT"]` and check length.

```python
sites = ["GAATTC", "AAGCTT"]
sites = sites + ["GGATCC"]
print(len(sites))  # prints 3
```

**Concept:** Demonstrates list concatenation and `len()` function.\
**Real-life Use:** Maintaining dynamic lists of restriction enzyme sites during cloning planning.

---

## 13. Mismatch Count

**Question:** Count mismatches at two positions between `s1 = "ATGC"` and `s2 = "ATGA"`.

```python
s1 = "ATGC"
s2 = "ATGA"
mismatches = 0
if s1[2] != s2[2]: mismatches += 1
if s1[3] != s2[3]: mismatches += 1
print('Mismatches:', mismatches)
```

**Concept:** Uses indexing and conditionals to compare specific positions.\
**Real-life Use:** SNP detection by comparing sequence reads at known variant sites.

---

## 14. Dictionary Add Entry

**Question:** Add "BamHI":"GGATCC" to `enzymes = {"EcoRI":"GAATTC"}`.

```python
enzymes = {"EcoRI": "GAATTC"}
enzymes['BamHI'] = 'GGATCC'
print('BamHI' in enzymes)
```

**Concept:** Illustrates adding key-value pairs to a dictionary.\
**Real-life Use:** Expanding enzyme lookup tables in bioinformatics scripts.

---

## 15. Protein Substring

**Question:** Check if substring "PEEK" is in `prot = "MVHLTPEEKSAVTALWGKV"`.

```python
prot = "MVHLTPEEKSAVTALWGKV"
if 'PEEK' in prot:
    print('Motif found')
else:
    print('Motif not found')
```

**Concept:** Uses substring membership test within a string.\
**Real-life Use:** Detecting functional motifs or domains in protein sequences.

---

## 16. First and Last Bases

**Question:** Print and compare `seq[0]` and `seq[-1]` in `seq = "ATGCGC"`.

```python
seq = "ATGCGC"
if seq[0] == seq[-1]:
    print('Same base at ends')
else:
    print('Different ends')
```

**Concept:** Demonstrates string indexing with positive and negative indices.\
**Real-life Use:** Verifying overhang compatibility in adapter sequences.

---

## 17. Palindromic Site

**Question:** Check if `site = "GAATTC"` is palindromic.

```python
site = "GAATTC"
if site == site[::-1]:
    print('Palindromic')
else:
    print('Not palindromic')
```

**Concept:** Uses slicing to reverse a string and compare equality.\
**Real-life Use:** Identifying restriction enzyme recognition sites.

---

## 18. Codon Tuple Access

**Question:** From `codons = ("AUG","UUU","UUC")`, retrieve the second element and compare to "UUU".

```python
codons = ("AUG", "UUU", "UUC")
print('Second codon is UUU' if codons[1] == 'UUU' else 'Mismatch')
```

**Concept:** Tuple indexing and inline conditional expression.\
**Real-life Use:** Extracting specific codons during manual translation checks.

---

## 19. Dictionary Keys List

**Question:** Get list of keys from `mw = {"Ala":89, "Gly":75}` and check if "Met" is present.

```python
mw = {"Ala":89, "Gly":75}
keys_list = list(mw.keys())
print('Met' in keys_list)
```

**Concept:** Converts dictionary keys view to a list and tests membership.\
**Real-life Use:** Ensuring required amino acids are included in molecular weight tables.

---

## 20. List Concatenation

**Question:** Concatenate `list1 = ["TP53","BRCA2"]` and `list2 = ["EGFR"]`, then check length.

```python
list1 = ["TP53", "BRCA2"]
list2 = ["EGFR"]
all_genes = list1 + list2
print(len(all_genes))  # prints 3
```

**Concept:** Uses list addition to merge lists and `len()` to count elements.\
**Real-life Use:** Combining gene panels for pathway enrichment analysis.

---

## 21. Case-Insensitive Gene Search

**Question:** Compare `gene = "brca1"` to `target = "BRCA1"` ignoring case.

```python
gene = "brca1"
target = "BRCA1"
print('Match' if gene.upper() == target else 'No match')
```

**Concept:** Normalizes strings to uppercase before comparison.\
**Real-life Use:** Standardizing input for database queries to avoid case mismatches.

---

## 22. Sequence Replace

**Question:** Replace "XX" with "AA" in `seq = "ATGCXXTA"` and check result.

```python
seq = "ATGCXXTA"
new_seq = seq.replace("XX", "AA")
print(new_seq)
```

**Concept:** Uses `str.replace()` to handle ambiguous placeholders.\
**Real-life Use:** Cleaning sequencing data by replacing ambiguous codes with known bases.

---

## 23. Tuple Unpacking

**Question:** Unpack `t = (45.2, 50.1, 48.3)` into `w1,w2,w3` and check if `w2 > 49`.

```python
t = (45.2, 50.1, 48.3)
w1, w2, w3 = t
print('Second >49' if w2 > 49 else 'Second <=49')
```

**Concept:** Demonstrates tuple unpacking and numeric comparison.\
**Real-life Use:** Processing replicate measurements from assays.

---

## 24. Set Difference

**Question:** Compute difference between `expected = {"AUG","GGC"}` and `observed = {"AUG","UUU","UAA"}`.

```python
expected = {"AUG", "GGC"}
observed = {"AUG", "UUU", "UAA"}
missing = expected - observed
print(missing)
```

**Concept:** Uses set subtraction to find elements in one set not in another.\
**Real-life Use:** Detecting missing codons in sequencing libraries.

---

## 25. Nested Dictionary Access

**Question:** Retrieve `pH` from `data = {"sample1": {"pH":7.4}}` and check if ≥ 7.

```python
data = {"sample1": {"pH":7.4}}
if data["sample1"]["pH"] >= 7:
    print('Neutral or alkaline')
else:
    print('Acidic')
```

**Concept:** Accesses values in nested dictionaries.\
**Real-life Use:** Extracting metadata parameters from structured sample records.

---

## 26. String Slicing for Codon

**Question:** Extract the second codon from `seq = "ATGGAACTT"` using slicing.

```python
seq = "ATGGAACTT"
codon = seq[3:6]
print(codon)  # prints 'GAA'
```

**Concept:** Applies slicing to isolate substring segments.\
**Real-life Use:** Manually retrieving specific codon sequences for analysis.

---

## 27. Dictionary Value Sum

**Question:** Sum counts from `counts = {"A":5, "T":3}` and check total == 8.

```python
counts = {"A":5, "T":3}
total = counts["A"] + counts["T"]
print('Total is 8' if total == 8 else 'Total is not 8')
```

**Concept:** Demonstrates retrieval of multiple dict values and arithmetic.\
**Real-life Use:** Computing nucleotide composition in sequence analysis.

---

## 28. Check GC-Rich Substring

**Question:** For `seq = "ATGCGCTAAG"`, check if substring from index 2–6 has ≥3 G+C.

```python
seq = "ATGCGCTAAG"
sub = seq[2:6]
if sub.count('G') + sub.count('C') >= 3:
    print('GC-rich segment')
else:
    print('Not GC-rich')
```

**Concept:** Combines slicing, `count()`, and conditional logic.\
**Real-life Use:** Identifying regulatory hotspots in promoter regions.

---

## 29. List Membership

**Question:** Check if "Thr" not in `amino = ["Ala","Gly","Ser"]`.

```python
amino = ["Ala", "Gly", "Ser"]
print('Thr absent' if 'Thr' not in amino else 'Thr present')
```

**Concept:** Uses list membership and negation in conditionals.\
**Real-life Use:** Verifying presence of phosphorylation sites in peptide lists.

---

## 30. Compare Two GC Contents

**Question:** Compare GC counts of `seq1 = "GGCCAA"` and `seq2 = "ATATAT"`.

```python
seq1 = "GGCCAA"
seq2 = "ATATAT"
gc1 = seq1.count('G') + seq1.count('C')
gc2 = seq2.count('G') + seq2.count('C')
print('seq1 is richer' if gc1 > gc2 else 'seq2 is richer or equal')
```

**Concept:** Calculates and compares numeric results from string operations.\
**Real-life Use:** Contrasting GC content between genomic regions.

---

## 31. Dictionary Update vs New Key

**Question:** Update `mw` with `mw['Ser']=105` and check if key existed before.

```python
mw = {"Ala":89, "Gly":75}
was_present = 'Ser' in mw
mw['Ser'] = 105
print('Ser existed' if was_present else 'Ser newly added')
```

**Concept:** Checks key presence before assignment.\
**Real-life Use:** Safely updating lookup tables without overwriting existing entries.

---

## 32. Tuple Concatenation

**Question:** Concatenate `t1 = ('A','T')` and `t2 = ('G','C')` and check length.

```python
t1 = ('A', 'T')
t2 = ('G', 'C')
t3 = t1 + t2
print(len(t3))  # prints 4
```

**Concept:** Demonstrates tuple addition and `len()`.\
**Real-life Use:** Building complete codon lists from partial data.

---

## 33. Set Symmetric Difference

**Question:** Compute symmetric difference between `s1 = {'AUG','UUU'}` and `s2 = {'UUU','AAG'}`.

```python
s1 = {'AUG', 'UUU'}
s2 = {'UUU', 'AAG'}
diff = s1 ^ s2
print(diff)
```

**Concept:** Uses the `^` operator to find elements unique to each set.\
**Real-life Use:** Identifying codon changes between wild-type and mutant sequences.

---

## 34. Validate IUPAC Code

**Question:** Check if `x = 'N'` is a valid IUPAC nucleotide code in `{'A','T','G','C','R','Y'}`.

```python
x = 'N'
valid = set('ATGCRY')
print('Valid' if x in valid else 'Invalid')
```

**Concept:** Tests membership in a set of allowed characters.\
**Real-life Use:** Filtering out unexpected ambiguity codes from sequence data.

---

## 35. Multiple-Choice Conditional

**Question:** Given `choice = 'qPCR'`, print different messages for 'PCR', 'qPCR', or others.

```python
choice = 'qPCR'
if choice == 'PCR':
    print('Standard PCR protocol')
elif choice == 'qPCR':
    print('Quantitative PCR protocol')
else:
    print('Unknown protocol')
```

**Concept:** Demonstrates `if`–`elif`–`else` branching.\
**Real-life Use:** Selecting lab protocols based on experimental method input.

---

## 36. Dictionary Length Check

**Question:** Check if `meta = {'id':1,'pH':7.4,'temp':37}` has 3 entries.

```python
meta = {'id':1, 'pH':7.4, 'temp':37}
print('Complete' if len(meta) == 3 else 'Incomplete')
```

**Concept:** Uses `len()` on a dictionary to count keys.\
**Real-life Use:** Validating that sample metadata entries are fully populated.

---

## 37. Extract Sample IDs

**Question:** From `labels = ['S1:100','S2:200']`, extract IDs before ':' and make a new list.

```python
labels = ['S1:100', 'S2:200']
ids = [label.split(':', 1)[0] for label in labels]
print(ids)
```

**Concept:** Splits strings and uses list comprehension for transformation.\
**Real-life Use:** Parsing sample labels from plate-reader outputs for downstream analysis.

---

## 38. Check Palindrome Protein

**Question:** Determine if `pep = 'MADAM'` is palindromic.

```python
pep = 'MADAM'
print('Palindromic' if pep == pep[::-1] else 'Not palindromic')
```

**Concept:** Reverses string via slicing and compares.\
**Real-life Use:** Identifying symmetric peptide sequences with potential structural motifs.

---

## 39. Replace Thymine with Uracil

**Question:** Convert `dna = 'ATGCTT'` to RNA by replacing 'T' with 'U'.

```python
dna = 'ATGCTT'
rna = dna.replace('T', 'U')
print(rna)
```

**Concept:** Uses `replace()` for character substitution in strings.\
**Real-life Use:** Transcribing DNA sequences to RNA sequences in silico.

---

## 40. Dictionary Key Exists

**Question:** Test if 'BRCA1' is a key in `genes = {'TP53':17, 'EGFR':7}`.

```python
genes = {'TP53':17, 'EGFR':7}
print('Present' if 'BRCA1' in genes else 'Absent')
```

**Concept:** Checks dictionary key membership.\
**Real-life Use:** Verifying gene annotation presence before further data retrieval.

---

## 41. Count Unique Amino Acids

**Question:** Count unique residues in `prot = 'MKTLLILAV'`.

```python
prot = 'MKTLLILAV'
unique_count = len(set(prot))
print(unique_count)
```

**Concept:** Converts string to set and counts elements.\
**Real-life Use:** Estimating sequence complexity and diversity.

---

## 42. Compare Two Lists by Sorting

**Question:** Check if `l1 = ['A','B','C']` and `l2 = ['C','B','A']` have same elements ignoring order.

```python
l1 = ['A','B','C']
l2 = ['C','B','A']
print(sorted(l1) == sorted(l2))
```

**Concept:** Uses `sorted()` to compare lists irrespective of element order.\
**Real-life Use:** Validating that different replicate runs yield identical gene hit lists.

---

## 43. Simple Boolean Flag

**Question:** Set `high_gc` to True if GC% of `seq = 'ATGCGC'` > 50%.

```python
seq = 'ATGCGC'
gc = (seq.count('G') + seq.count('C')) / len(seq) * 100
high_gc = gc > 50
print(high_gc)
```

**Concept:** Calculates percentage and assigns boolean flag.\
**Real-life Use:** Flagging sequences for special handling based on GC content thresholds.

---

## 44. Tuple to List and Back

**Question:** Convert `t = ('A','T','G')` to list, mutate index 1, then back to tuple.

```python
t = ('A','T','G')
_lst = list(t)
_lst[1] = 'C'
t_new = tuple(_lst)
print(t_new)
```

**Concept:** Demonstrates type conversion between tuple and list.\
**Real-life Use:** Editing immutable sequence fragments programmatically.

---

## 45. Dictionary Key Rename

**Question:** Rename key 'old' to 'new' in `d = {'old':1}`.

```python
d = {'old':1}
value = d.pop('old')
d['new'] = value
print(d)
```

**Concept:** Uses `pop()` to remove and retrieve before reassigning.\
**Real-life Use:** Standardizing metadata field names across datasets.

---

## 46. Check Even-Length Sequence

**Question:** Print “Even” if `seq = 'ATGCGA'` has even length.

```python
seq = 'ATGCGA'
print('Even' if len(seq) % 2 == 0 else 'Odd')
```

**Concept:** Uses `len()` and modulo to test parity.\
**Real-life Use:** Validating barcode or adapter sequence lengths for library prep.

---

## 47. Merge Two Dicts

**Question:** Combine `d1 = {'A':1}` and `d2 = {'B':2}` into `d3`.

```python
d1 = {'A':1}
d2 = {'B':2}
d3 = {**d1, **d2}
print(d3)
```

**Concept:** Uses dictionary unpacking for merging.\
**Real-life Use:** Integrating multiple annotation sources into a single lookup map.

---

## 48. Validate Codon Alphabet

**Question:** Ensure each char in `codon = 'ATG'` is in `{'A','T','G','C'}`.

```python
codon = 'ATG'
valid_bases = set('ATGC')
print(all(c in valid_bases for c in codon))
```

**Concept:** Tests all elements for membership using `all()`.\
**Real-life Use:** Sanity-check user-provided codon sequences before analysis.

---

## 49. Compare Two Dictionaries

**Question:** Check if `d1 = {'x':1,'y':2}` and `d2 = {'y':3,'x':4}` have identical key sets.

```python
d1 = {'x':1, 'y':2}
d2 = {'y':3, 'x':4}
print(set(d1.keys()) == set(d2.keys()))
```

**Concept:** Compares key sets of dictionaries for equality.\
**Real-life Use:** Verifying consistent annotation fields across sample metadata.

---

## 50. Conditional Nested Dict Creation

**Question:** Create `{'gene':gene,'status':...}` based on `exp` > 1.0.

```python
gene = 'TP53'
exp = 1.2
result = {'gene': gene, 'status': 'up' if exp > 1.0 else 'down'}
print(result)
```

**Concept:** Combines inline conditional with dictionary literal creation.\
**Real-life Use:** Generating result objects for differential expression reports.

