# Android_Janken
書籍『はじめてのAndroidプログラミング』第５章じゃんけんアプリの実装です。  

<img src="https://user-images.githubusercontent.com/37995730/49918147-62010500-fee5-11e8-877c-c2fe6726649f.png" width="320px"> <img src="https://user-images.githubusercontent.com/37995730/49918151-662d2280-fee5-11e8-8201-1cb8b5b52272.png" width="320px">


## 学習メモ  
●画面推移についての理解を進めた。  

・Activityの推移にIntentを利用。  
・制作の流れは「Layout」 --> 「Activity」。　Unityの様な流れ、画面に空のオブジェクトをID振って置いてゆくイメージ。   
・Kotlinはスッキリしてて良さげ。  
・少量のデータ保存に、共有プリファレンスが利用できる。データベースを利用した保存方法は本書最後のアプリで解説される。  
・Androidの基本動作の流れであるActivityのライフサイクルについて理解。言葉より図の方がイメージしやすいのでメモ。
<img src="https://developer.android.com/images/activity_lifecycle.png" width="320px">  
※ https://developer.android.com/reference/android/app/Activity#ActivityLifecycle  
今回はActivityが二つ。MainとResult。  
Result側で、onDestroy()としてfinish()が呼ばれている。リファレンス参照。  
以下に全体の流れをメモとして記述  
MainActivity： onCreate ==> startActivity(Result) ==> ResultActivityへ  
ResultActivity: onCreate ==> finish() ==> MainActivityへ  

つまりMainActivityはonStopもonDestroyもされず起動したままの様子。
