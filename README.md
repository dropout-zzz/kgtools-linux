# kgtools
Used to extract .kg files from SystemC Engine

## building with cmake

a bit cursed i havent yet tried to fix it:

1. build in-tree to generate some headers. it will error on linux and macos because output executable conflict with folder name
2. build again but set a build dir. so it make uses the header and avoids errors
