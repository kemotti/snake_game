# snake_game
macOS上で動作するc言語を用いて作成したスネークゲームです。コンパイルしていただき実行してください。
termios.h ヘッダーファイルと関連する関数 _kbhit()、_getch()、usleep() を使用して、macOSでのキー入力とタイミングの制御を行っています。また、system("clear") を使用してターミナルをクリアし、画面を更新しています。コードをコンパイルして実行すると、ゲームが開始されます。スネークの動きを "W"（上）、"A"（左）、"S"（下）、"D"（右）キーで制御し、スコアを表示します。⚪︎が操作するものでFと書かれた敵を取り込みながら高得点を狙います。壁に当たると強制的にゲームが終了するのでお気をつけください。ゲームが終了すると、最終スコアが表示されます。
コンパイルするには保存していただき、terminalにて
gcc snake_game.c -o snake_game
を打ち込んでください。
そのあとは
./snake_game
と入力してゲームを実行できます。
問題点はグラフィックが弱いこと、操作性が少し悪いこと動きが少ないことが挙げられます。
解決策はグラフィックライブラリやフレームワークを使用することやキーボード操作の改善: ゲーム内のキーボード操作をより直感的にし、反応性を高めることが重要であり、キーボード入力を即座に受け付けるために、非バッファ入力モードを使用することができそうです。
マウスサポートの追加: マウス操作をゲームに組み込むことで、操作性を向上させることができ、マウスによるポインタの位置検出やクリックイベントの処理を行うことで、より直感的な操作が可能になると思われます。

ゲームパッドのサポート: SDLやAllegroなどのゲーム開発用ライブラリを使用すると、ゲームパッドの入力を処理でき、ゲームパッドのボタン配置やアナログスティックの操作をゲームに適切に組み込むことで、よりリアルな操作感を実現できると思います。

ユーザーインターフェースの改善: ゲーム内のメニューやオプション画面などのユーザーインターフェースを改善することも操作性向上に貢献しそうでした。情報を明確に表示し、操作方法を分かりやすく案内することで、プレイヤーがゲームをスムーズに操作できるようになると思います。
