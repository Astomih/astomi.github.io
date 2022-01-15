---
layout: home
title: HOMEPAGE
subtitle: 惰性的な日々
---

# ブログ
[astomih.hatenablog.com](https://astomih.hatenablog.com/)  
# ツイッター
[@astomih](https://twitter.com/Astomih)  
# GitHub
[GitHub](https://github.com/Astomih)  
# メール
astomih.jp@gmail.com


# 作っているもの
## sinen
C++20がメインのWindows/Linux/Android/Webに対応中のVulkan/OpenGLバックエンドな2D/3Dライブラリ
 
[https://github.com/astomih/sinen](https://github.com/astomih/sinen)  
  
[APIリファレンス](https://astomih.github.io/sinen)  
  
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

## 開発コード：utilis
開発中

# 作ったもの
取り敢えずGitHubにまとめています。  
[https://github.com/astomih/Works](https://github.com/astomih/Works)  

## Wall Avoid
![WallAvoid]({{site.baseurl}}/assets/img/wall_avoid.png)

## 念打
![Nenda]({{site.baseurl}}/assets/img/Nenda.png)