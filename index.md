---
layout: home
title: Astomihの部屋
subtitle: 惰性的な毎日
---

# 自己紹介
大学生です。アニメとかゲーム観たりやったりしています。アニメ：ゲーム：プログラム＝６：３：１  
  
# 技術ブログ
[https://astomih.hatenablog.com/](https://astomih.hatenablog.com/)  
ほとんど書かない技術ブログ  
# ツイッター
[@Astomih](https://twitter.com/Astomih)  
# GitHub
[GitHub](https://github.com/Astomih)  
# メール
astomih.jp@gmail.com


# 作っているもの
## NenEngine
C++20がメインのWindows/Android/Webに対応中のVulkan/OpenGLバックエンドな2D/3Dライブラリ(長い)
 
[https://github.com/astomih/NenEngine](https://github.com/astomih/NenEngine)  
  
[APIリファレンス](https://astomih.github.io/NenEngine)  
  
### コード例
``` c++
#include <Nen/Nen.hpp>

/**
 *  メインシーン
 * データメンバが定義出来ないので、
 * 基本的に各種設定を行って他のシーンに移るための踏み台となる
*/
void Main::Setup()
{
    //背景を黒に設定
    GetRenderer()->SetClearColor(nen::Palette::Black);

    //フォントの読み込み
    auto font = std::make_shared<nen::Font>();
    font->LoadFromFile("Assets/Font/mplus/mplus-1p-medium.ttf", 72);

    //アクターを追加
    auto actor = this->AddActor<nen::Actor>();

    //アクターにコンポーネントを追加
    auto text = actor->AddComponent<nen::TextComponent>();
    text->SetFont(font);
    text->SetString("Hello,World!", nen::Palette::White);
}

void Main::Update(float deltaTime)
{
    //キーボードのQが押されたら終了
    if (GetInput().Keyboard.GetKeyValue(nen::KeyCode::Q))
        Quit();

    /**
     * 描画処理は裏側で行っている
    */
}
```
結果：
![結果]({{site.baseurl}}/assets/img/result.png)

# 作ったもの
取り敢えずGitHubにまとめています。  
[https://github.com/astomih/Works](https://github.com/astomih/Works)  

## Wall Avoid
 赤い壁を避けながらコインを集める的なゲームです。  
 高校の頃にUnityで初めて作りました。大学の課題にもそのまま出しました。万能です。
![WallAvoid]({{site.baseurl}}/assets/img/wall_avoid.png)

## 念打
 ひたすら降ってくる球をひたすら撃つゲームです。やる気が出ませんでしたわ。  
 正直一ミリも面白く無いです。何故作ったのだろうか。  
 またSTGを作る気力が出たらこいつを土台にして作ろうと思います。
![Nenda]({{site.baseurl}}/assets/img/Nenda.png)
 