# find_duplicates.py

This script is a file duplicate detection tool
that identifies duplicate files in specified directories.
It uses a combination of file size, partial file hash (first 1 KB),
and full file hash to efficiently detect duplicates.

Here's an overview of its functionality:

The check_for_duplicates() function orchestrates the workflow:

- Lists all files in the specified directories.
- Filters files step-by-step (by size, first 1 KB hash, and full hash) to detect duplicates.
- Prints the detected duplicates.

### How It Works:

Users run the script with one or more directory paths as arguments.
The script progressively narrows down duplicate candidates:
Files with unique sizes are excluded early.
Files with matching sizes are further checked using a partial hash.
Final duplicate confirmation is done by comparing full content hashes.
The results (duplicate groups) are printed to the console.
Use Case:
This tool is ideal for:

Finding duplicate files to free up disk space.
Comparing files across multiple directories.
Handling large datasets efficiently by reducing the need for full file comparisons upfront.
