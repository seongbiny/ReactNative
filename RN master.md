## The Rules of Native

* RN은 웹사이트가 아니다.
  * HTML이 아니기 때문에 div는 쓸 수 없다. 대신 `View`를 사용 항상 `View` import 하기! View = Container 
* RN에 있는 모든 text는 text component에 들어가야 한다.
  * 브라우저가 아니기때문에 span, p 등등 사용 못함. 대신 `Text` component 사용
* \<View style={styles.container}>
  * style 속성도 웹에서 사용하던 모든 것을 사용할 수는 없다.
  * StyleSheet.create 사용하면 자동완성 기능 있음



* 모든 View 들이 기본적으로 Flex Container
* RN에서는 Flex Direction의 기본값은 Column NOT row!
* aa
