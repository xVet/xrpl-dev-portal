XRP Ledger内の多くのオブジェクト、特にトランザクションとレジャーは、256ビットのハッシュ値で一意に識別されます。通常、この値は「SHA-512ハーフ」として算出されます。SHA-512ハーフは、あるコンテンツから[SHA-512](http://dx.doi.org/10.6028/NIST.FIPS.180-4)ハッシュを計算し、出力の前半を取得したものです。（これは256ビット、つまり32バイトで、16進数表記では64文字です。）オブジェクトのハッシュは、極めて競合の発生しにくい方法でコンテンツから生成されるため、2つのオブジェクトが同じハッシュを持つ場合、それらのオブジェクトは同じものと見なされます。

XRP Ledgerのハッシュ値には、以下の特徴があります。

* 長さは64文字ちょうどです
* [16進数](https://en.wikipedia.org/wiki/Hexadecimal)の文字セット: 0-9およびA-Fです。
* 通常は大文字で記述されます。

{% admonition type="info" name="注記" %}SHA-512ハーフは、公式に定義されている _SHA-512/256_ ハッシュ関数とほぼ同等のセキュリティーを持ちます。しかし、XRP LedgerはSHA-512/256より前から利用されているため、既存のSHA-512関数上に実装することも容易にできます。（この記事の時点で、暗号ライブラリーでのSHA-512のサポートはSHA-512/256よりはるかに一般的です。）{% /admonition %}
