```
units:
  kx: cx
  ky: cy
  px: kx + 2
  py: ky + 2
  num: 6*2*5-1
points:
  zones:
    matrix:
      columns:
        outer:
        pinky:
        ring:
        middle:
        index:
        inner:
          rows.mod.skip: true
      rows:
        mod:
        bottom:
        home:
        top:
        num:
    extras:
      key:
        padding: 1ky
        spread: 1kx
      anchor:
        ref: matrix_inner_mod
        shift: [kx/2 + .5, 0]
      columns:
        l1:
          key:
            width: 2kx
      rows:
        cluster: 
  mirror: &mirror
    ref: matrix_inner_home
    distance: kx+1
outlines:
  raw:
    - what: rectangle
      where: true
      size: [px, py]
  keys:
    - what: rectangle
      where: true
      size: [kx-0.5,ky-0.5]
  board:
    - what: rectangle
      where: true
      size: [1.5px, 1.5py]
  combo:
    - name: board
    - operation: subtract
      name: keys    
```