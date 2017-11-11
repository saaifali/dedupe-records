# Dedupe Examples



### [Record Linkage example](https://dedupeio.github.io/dedupe-examples/docs/record_linkage_example.html) -  electronics products
This example links two spreadsheets of electronics products and links up the matching entries. Each dataset individually has no duplicates.

```bash
cd record_linkage_example
python record_linkage_example.py
```

**To see how you might use dedupe for linking datasets, see the [annotated source code for record_linkage_example.py](https://dedupeio.github.io/dedupe-examples/docs/record_linkage_example.html).**


## Training

The _secret sauce_ of dedupe is human input. In order to figure out the best rules to deduplicate a set of data, you must give it a set of labeled examples to learn from.

The more labeled examples you give it, the better the deduplication results will be. At minimum, you should try to provide __10 positive matches__ and __10 negative matches__.

The results of your training will be saved in a JSON file for future runs of dedupe.

Here's an example labeling operation:

```bash
Phone :  2850617
Address :  3801 s. wabash
Zip :
Site name :  ada s. mckinley st. thomas cdc

Phone :  2850617
Address :  3801 s wabash ave
Zip :
Site name :  ada s. mckinley community services - mckinley - st. thomas

Do these records refer to the same thing?
(y)es / (n)o / (u)nsure / (f)inished
```
