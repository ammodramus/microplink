`microplink`
===========

This class provides a minimal and fast interface for retrieving genotypes
from Plinks's BED/BIM/FAM file trios. The BED file must fit in memory.

Requirements
------------

`numpy`, `pandas`, and `numba`. These are included with many Python
distributions.

Installation
------------

Run `pip install microplink` or clone this repository and run

```
python setup.py install
```

Usage
-----

Typical usage:

    pf = PlinkFiles('test.bed', 'test.bim', 'test.fam')

    # fetch by chromosome and position
    pf.get_genotypes(chromosome=1, position=10000)

    # fetch by variant name (often RSID)
    pf.get_genotypes(snp='rs1235123')

    # fetch by SNP integer index
    pf.get_genotypes(snp_index=0)
