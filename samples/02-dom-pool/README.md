# 02-dom-pool
**Goal**: DOM生成/破棄をやめ、再利用（プール化）で軽くする。  
**How**: `index.html` を開く。  
**Key points**:
- 初期に要素をN個作る → 以後は位置だけ更新
- `top/left`ではなく`transform`でレイアウト無効化を回避
- Firefox Performance で Layout/DOM が小さくなるのを確認
