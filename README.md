# 知覚キットの取付位置 (3D プレビュー)

https://r-okauchi.github.io/perception-kit-mounts/

油圧ショベル zx200 とクローラダンプ mst110cr の機体モデルに、後付けの知覚キット (屋根 LiDAR・IMU・GNSS バー、
zx200 は右の手すりの Airy) の治具と留め具を、決めた取付位置で載せたもの。three.js (CDN) で描く静的なページ。

- `index.html`: ページ
- `meshes/<機体>.bin`: 三角形 (頂点ごとに Int16 ×3、リトルエンディアン、機体の箱で量子化)。並びと箱は `index.html` の
  `mesh-index`

## 機体モデルの出典

`meshes/*.bin` の機体部分 (上部旋回体・作業機・荷台・足回り) は
[OperaSim-PhysX](https://github.com/pwri-opera/OperaSim-PhysX) (Copyright 2022 Public Works Research Institute, Japan)
の `Assets/Machines/zx200`・`Assets/Machines/mst110cr` を変換したもの (走行姿勢に組み、キットの hub 系に移し、16 bit に
量子化)。Apache License 2.0 に従う: [LICENSE-OperaSim-PhysX.txt](LICENSE-OperaSim-PhysX.txt)。
