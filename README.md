# Compressor
Lossless data compressor built in C.

## Pipeline
1. **BWT** (Burrows-Wheeler Transform) — sorts data to improve compressibility
2. **MTF** (Move-to-Front) — reduces entropy by tracking symbol recency  
3. **Huffman Coding** — variable-length encoding for final compression

For compressing-
"gcc -O2 -std=c11 main.c main_huffman.c main_rle.c main_bwt.c main_mtf.c -o compressor"
compressor.exe

For decompressing-
"gcc -O2 -std=c11 decompress.c main_huffman.c main_rle.c main_bwt.c main_mtf.c -o decompressor"
decompressor.exe
