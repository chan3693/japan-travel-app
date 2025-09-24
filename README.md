# japan-travel-app\
│\
├── android/                # Android 原生專案文件\
├── ios/                    # iOS 原生專案文件\
├── app/                    # App 核心程式碼\
│   ├── components/         # 可重用 UI 組件\
│   │   ├── Button.js\
│   │   ├── Card.js\
│   │   └── Carousel.js\
│   │\
│   ├── screens/            # 各個頁面\
│   │   ├── HomeScreen/\
│   │   │   ├── index.js\
│   │   │   └── styles.js\
│   │   ├── PlaceDetailScreen/\
│   │   │   ├── index.js\
│   │   │   └── styles.js\
│   │   ├── PlanTripScreen/\
│   │   │   ├── index.js\
│   │   │   └── styles.js\
│   │   ├── LoginScreen/\
│   │   └── CalendarScreen/\
│   │\
│   ├── navigation/         # React Navigation\
│   │   ├── AppNavigator.js\
│   │   └── AuthNavigator.js\
│   │\
│   ├── redux/              # 狀態管理 (可用 Redux Toolkit)\
│   │   ├── store.js\
│   │   └── slices/\
│   │       ├── userSlice.js\
│   │       └── tripSlice.js\
│   │\
│   ├── services/           # API / 資料處理\
│   │   ├── api.js\
│   │   └── firebase.js\
│   │\
│   ├── utils/              # 工具函數\
│   │   ├── helpers.js\
│   │   └── constants.js\
│   │\
│   ├── assets/             # 圖片 / 字型 / icon\
│   │   ├── images/\
│   │   └── fonts/\
│   │\
│   └── App.js              # React Native 入口文件\
│\
├── package.json\
├── babel.config.js\
├── metro.config.js\
└── README.md


架構說明

app/components/

放可重用 UI 元件，例如按鈕、卡片、Carousel、Header 等

app/screens/

每個頁面單獨資料夾

index.js：頁面邏輯與 JSX

styles.js：頁面樣式

app/navigation/

React Navigation 的 Stack / Tab Navigator

AppNavigator.js → 登入後主頁面導航

AuthNavigator.js → 登入/註冊流程導航

app/redux/

全局狀態管理

store.js：Redux store

slices/：各個功能 slice（user、trip、favorites）

app/services/

API 調用封裝

firebase.js：Firebase Auth / Firestore 封裝

app/utils/

常用工具函數 / 常量

helpers.js：格式化日期、計算距離等

constants.js：城市列表、顏色、字體定義

app/assets/

圖片、icon、字型等資源

images/：景點圖、背景圖

fonts/：自定義字體

App.js

程式入口

加載 Provider (Redux) + NavigationContainer
