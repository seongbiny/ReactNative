# React Native

## 개발 환경 준비하기

> 리액트 네이티브를 개발하기 위해 Node.js, JDK, 안드로이드 스튜디오를 설치해야한다. 

1. Expo 설치

```bash
$ npm install -g expo-cli
```

```bash
$ expo init my-first-expo
```

## 컴포넌트

### JSX     

* 하나의 부모로 감싸야한다
* <View> 는 <div>, <Fragment> 와 비슷함

### if 조건문

> 복잡한 조건인 경우 JSX 밖에서 조건에 따른 값을 설정하고 JSX 내에서 사용하는 조건문은 최대한 간단하게 작성
>
> JSX 내부에서 if문을 사용하려면 즉시실행함수 형태로 작성해야 함

```jsx
...
export default function App() {
    const name = 'Seongbin';
    return (
    <View style={styles.container}>
    	<Text style={styles.text}>
            {(() => {
                if (name === 'Hanbit') return 'My name is Hanbit';
                else if (name === 'Seongbin') return 'My name is Seongbin';
                else return 'My name is React Native';
            })()}
        </Text>
        <StatusBar style="auto" />
    </View>
  );
}
...
```

#### 삼항 연산자

```jsx
...
export default function App() {
    const name = 'Seongbin';
    return (
    	<View style={styles.container}>
        	<Text style={styles.text}>
            	My name is {name === 'Seongbin' ? 'Seongbin Yun' : 'React Native'}
            </Text>
            <StatusBar style="auto" />
        </View>
    );
}
...
```

#### AND 연산자와 OR 연산자

```jsx
...
{name === 'Seongbin' && (
 <Text style={styles.text}>My name is Seongbin</Text>
 )}
{name !== 'Seongbin' && (
 <Text style={styles.text}>My name is not Seongbin</Text>
)}
...
```

#### null과 undefined

조건에 따라 출력하는 값을 변경하다 보면 컴포넌트가 null이나 undefined를 반환하는 경우가 있다. JSX는 null은 허용하지만 undefined는 오류가 발생한다.

### 컴포넌트

> 재사용이 가능한 조립 블록으로 화면에 나타나는 UI 요소

#### 내장 컴포넌트

[리액트 네이티브 컴포넌트](https://reactnative.dev/docs/components-and-apis)

#### 커스텀 컴포넌트 만들기

```jsx
import React from 'react';
import { TouchableOpacity, Text } from 'react-native';

const MyButton = () => {
    return (
    	<TouchableOpacity>
        	<Text style={{ fontSize: 24 }}>My Button</Text>
        </TouchableOpacity>
    );
};

export default MyButton;
```

### props와 state

#### Pressable 컴포넌트

리액트 네이티브 0.63 버전부터 기존의 `TouchableOpacity` 컴포넌트를 대체하는 `Pressable` 컴포넌트가 추가됨

사람마다 손의 크기나 두께가 모두 다르기 때문에 누군가는 버튼을 정확하게 클릭하는 것이 어려울 수 있다. 이런 상황을 해결하기 위해 버튼 모양보다 약간 떨어진 부분까지 이벤트가 발생할 수 있도록 `Pressable` 컴포넌트에서는 `HitRect`를 이용해 설정을 쉽게 할 수 있다.

## 스타일링

### styled-components

## React Navigation

* 리액트 네비케이션 라이브러리 설치

```bash
$ expo init react-native-navigation
```

* 사용하는 네비게이션의 종류에 따라 개별적으로 추가 라이브러리를 설치

```bash
$ expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
```

### navigation 종류

* stack
* tab
* drawer

### navigation

* NavigationContainer 컴포넌트
  * 네비게이션의 계층 구조와 상태를 관리하는 컨테이너 역할을 하며 네비게이션의 모든 구조를 감싸는 최상위 컴포넌트이다.
* Navigator 컴포넌트
  * 화면을 관리하는 중간 관리자 역할로, 네비게이션을 구성하며 여러 개의 Screen 컴포넌트를 자식 컴포넌트로 갖는다.
* Screen 컴포넌트
  * 화면으로 사용되는 컴포넌트로 name속성과 component 속성을 지정해주어야 한다.

#### stack navigation

```bash
$ npm install @react-navigation/stack
```



9/8 1주차 수업 완료
