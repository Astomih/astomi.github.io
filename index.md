---
layout: home
title: Astomihの部屋
subtitle: 惰性的な毎日
---

# 自己紹介
大学生です
  
# 技術ブログ
[https://astomih.hatenablog.com/](https://astomih.hatenablog.com/)  
ほとんど書かない技術ブログ  
# Twitter
[@Astomih](https://twitter.com/Astomih)  
# GitHub
[GitHub](https://github.com/Astomih)  
# E-Mail
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

 