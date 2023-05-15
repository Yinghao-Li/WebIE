# Shopping Interested-Related Product Type Mining Dataset

This folder contains the annotated dataset for the product type (PT) extraction task.

## Annotated HTML DOM trees

The annotated DOM trees are in the `./csv/` folder.
Each `.csv` file defines one DOM tree.
The attributes include
- `node_id`: the index of the current node.
- `parent_id`: the index of the parent of the current node; the root node has no parent id.
- `tag`: the HTML tag of each node.
- `text`: the text sequence within each tag.
- `label`: the label of each node; "y" indicates that the node text is a PT phrase while "n" indicates the opposite.

## Metadata

The file `./meta.csv` defines the shopping interest (concept) associated with each DOM tree.
In addition, it also provides the URL of the original webpage

## Dataset splits

We randomly split the data points *by shopping interest (concept)* into training, validation and test datasets.
We take 5 random runs and store the results into `./split-*.json` files.

## Data License

The WebPT dataset is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
