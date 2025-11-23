# pytorch autoencoder on MNIST

## 概要
エンコーダー、デコーダーの仕組みを理解するために画像の圧縮と復元の実験を行いました。特に２次元空間における表現能力の限界を検証しました。
## 設計
- 全結合層のみ
- 全結合層を畳み込み層に置き換え
- さらにノイズ除去を導入

mnistの画像が28 ＊ 28 * 1のテンソル。これを全結合層、畳み込み層を用いて2次元に圧縮。これに対して逆演算を行い、元の28 * 28 * 1のサイズに戻す。このデコードされたものとオリジナルをmaeを評価指標として比較し、これを最小化するように最適化した。

## 結果
以下の画像は２次元に圧縮した画像の２次元空間での位置を数字の関係性を可視化したものです。</br>
全結合層のみ</br>
<img width="774" height="836" alt="Unknown-5" src="https://github.com/user-attachments/assets/2ff5f69d-38a1-4af3-896b-1964aa560d7e" />

　</br>
畳み込み層</br>
<img width="763" height="836" alt="Unknown-7" src="https://github.com/user-attachments/assets/3c917ad0-ed89-422f-a520-4abb30445146" />

 </br>
ノイズ除去</br>

<img width="774" height="836" alt="Unknown-9" src="https://github.com/user-attachments/assets/b16d5b4a-01dc-4966-b79c-d2f187cb0fc1" />

