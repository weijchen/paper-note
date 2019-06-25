# Neural Machine Translation by Jointly Learning to Align and Translate
## 作者: Dzmitry Bahdanau, Kyunghyun Cho, Yoshua Bengio

## 研究目的
    * 為了解決 auto-encoder 在處理 fixed-length vector 時的問題，特別在長句子的 case

## 研究方式
    * 提出稱為 (soft-)alignments 的方式 -> learns to align and translate jointly
        - 每次翻譯的時候 (generate a word in a translation)，(soft-)search 句子中最相關的位置
        - Encodes the input sentence into a sequence of vectors and chooses a subset of these vectors
            + 123
    * 英文對法文的翻譯問題
    * Encoder-Decoder (via RNN):
        - 透過當下的 input 以及前一個時間點的 hidden state 來定義當下的 hidden state
        - 再透過一個 nonlinear function 來轉換所有的 hidden state 成 context vector c

    * 最後將 c 以及過往所 predict 的字 (y 集合) 進行轉換，求出機率最高的結果

    * Proposed approach: 
        - Encoder - Bidirectional RNN
        - Decoder - 
## 研究貢獻