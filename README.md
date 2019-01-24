# scrubadub
parses, cleans, and expands addresses for consistency + good geocoding

These scripts:
* Must be run in a particular order: `parse_<dataset name>.ipynb`, then either of the others, depending on your needs.
* Are designed to standardize our purchased datasets. One is from CoStar, and the second is from the National Establishment-Level Time Series. I've made some fake datasets with identical schemas to the purchased data to show the required format and the script's capabilities
* Are a work in progress. Next fixes include adjustments for:
  - South, North, East, and West Streets (currently, these will be incorrectly replaced with S St, N St, etc.). The same applies with South, North, East, and West Avenues.
  - Reducing redundancies in regular expressions if possible. Currently, each exception is exhaustively enumerated.
  - Smarter use of data structures if possible. Too many flat lists.
  - Prompt user to locate input file. Better yet, prompt user to locate input file and identify columns needed for identification and parsing.
  - Other inevitable oversights: dropping useful input information, etc.
