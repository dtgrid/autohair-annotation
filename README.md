# autohair-annotation
    
1. 髪方向作成手法: 
    1. labelmeというソフトを使う
    
        [インストールと使い方はこちらを参考](https://github.com/wkentaro/labelme) 

        1. `./masked_hairs` からマスクオーバーレイ画像を読み取る．
            <img width="400" src="for_readme/labelme_1.png"/>
        2. polygonで各髪領域を書いて，ラベルをつける (0,1,2,...整数を使ってください).
            <img width="400" src="for_readme/labelme_2.png"/>
        3. lineで各髪領域の方向を表す：
            - lineの原点が矢印の原点とみなして線を描く.
            - 対象髪領域と同じラベルをつける. **<== 大事**
            <img width="400" src="for_readme/labelme_3.png"/>
            <img width="400" src="for_readme/labelme_4.png"/>
            <img width="400" src="for_readme/labelme_5.png"/>
        4. jsonファイルを`./points_json/'へ保存する．
