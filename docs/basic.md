# Basic knowledge

## Audio file format

### Summary

- [**パルス符号変調（PCM）**](https://ja.wikipedia.org/wiki/%E3%83%91%E3%83%AB%E3%82%B9%E7%AC%A6%E5%8F%B7%E5%A4%89%E8%AA%BF)
  - 波形のアナログ信号の振幅値をそのままデジタル信号に変換（標本化・量子化を行う）
    - cf. [サンプリング定理](https://ja.wikipedia.org/wiki/%E6%A8%99%E6%9C%AC%E5%8C%96%E5%AE%9A%E7%90%86)，[量子化誤差](https://ja.wikipedia.org/wiki/%E9%87%8F%E5%AD%90%E5%8C%96%E8%AA%A4%E5%B7%AE)
  - 非圧縮：リニアPCM，圧縮：色々
- [**パルス密度変調（PDM）**](https://ja.wikipedia.org/wiki/%E3%83%91%E3%83%AB%E3%82%B9%E5%AF%86%E5%BA%A6%E5%A4%89%E8%AA%BF)
  - 正の振幅値が大きいほど1の出現率が高くなるように符号化

- ファイルフォーマット：音声データをファイルに格納する形式に関する仕様
- コーデック：生の音声データを符号化 / 複合する方式

### 種類

特にPCM形式のもので目ぼしいものを列挙する．

当然だが，非圧縮は特別な処理が必要ない代わりにファイルサイズが大きくなり，
圧縮する場合ファイルサイズが小さくなるが圧縮する手間が発生するというトレードオフがある．

- 非圧縮音声
  - [**WAV（FIFF waveform Audio Format）**](https://ja.wikipedia.org/wiki/WAV)
    - Windowsにおける標準的な格納方式
    - 任意のサンプリング周波数とビットレートの音声を格納可能
    - 他の音声コーデックも格納可能
  - [**AIFF（Audio Interchange File Format）**](https://ja.wikipedia.org/wiki/AIFF)
    - Appleにおける標準的な格納方式
    - 圧縮音声も記録可能
  - [**BWF（Broadcast Wave Format）**](https://ja.wikipedia.org/wiki/Broadcast_Wave_Format)
    - 映画やテレビでよく用いられる
- 非可逆圧縮音声
  - 可聴域にない音や別の音にマスクされるような音などを省略する
  - [**AAC（Advanced Audio Coding）**](https://ja.wikipedia.org/wiki/AAC)
    - MP3よりも音質（圧縮効率）が良い
    - MPEG-2およびMPEG-4の仕様の一部として標準化（両規格でほぼ違いはない）
    - 拡張子：mov，mp4，m2ts，m4a，m4b，m4p，3gp，3g2またはaac
    - AirPodsとかに使われている
  - [**mp3**](https://ja.wikipedia.org/wiki/MP3)
    - 音楽ダウンロード配信で最も一般的な音声非可逆圧縮コーデック
    - MPEG-1のオーディオ規格として開発された
    - 著作権保護のためのセキュア規格が存在する
  - [**mp4**](https://ja.wikipedia.org/wiki/MP4)/[**m4a**](https://ja.wikipedia.org/wiki/MP4)
    - 動画ストリームや字幕なども格納可能（音声の中身はAACであることも多い）
- 可逆圧縮音声
  - 省略（[TAK](https://ja.wikipedia.org/wiki/TAK)や[FLAC](https://ja.wikipedia.org/wiki/FLAC)などが有名な気がする）
