# 03-canvas-batch-raf
**Goal**: 受信は多くても、描画は「100msごとに最新だけ」をまとめ反映。  
**How**: `index.html` を開く。  
**Key points**:
- データは常に `latest` に上書き（古いキューは捨てる）
- rAFは60FPSで回しつつ、描画は100msごとにスロットリング
- DOMはCanvas 1枚なので Layout 負荷が激減
