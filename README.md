# wm2023_34
東大松尾研講義「世界モデルと知能2023」最終課題用のリポジトリです．


## タイトル
LLMによるプランニングの知識グラフによる拡張

## 概要
大規模言語モデル（LLM）は様々なタスクにおいて高い性能を達成するが，論理的推論やプランニングの能力は十分とは言い難い．これはLLMが逐次的にトークンを出力する仕組みであり，内部に現実環境を反映した世界モデルを保持していないためだと指摘されている．先行研究として，LLMを環境ダイナミクスを表現する世界モデルとみなしてプランニングを行うRAP-MCTSと呼ばれるアプローチが存在し[Hao+, 2023]，ブロックの並び替えなどの推論・プランニングタスクで高い性能を誇っている．しかしながら，この手法では状態の表現がテキストベースであり実環境との接地ができていないという課題が考えられる．そこで本研究では，Graph Neural Prompting[Tian+, 2023]を用いて，テキストで表現された状態と，オブジェクト間関係性を表現した知識グラフを結びつける手法を試みている．知識グラフの埋め込み表現を獲得したうえでLLMにプロンプトとして付与させることで現実環境と接地させ，プランニングの性能を改善する．