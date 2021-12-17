# vue-advanced

1. 기본적인 컴포넌트 등록과 컴포넌트 통신  
2. slot - 마크업 확장이 가능한 컴포넌트  
3. controlled - 결합력이 높은 컴포넌트  :  
서드파티 라이브러리, 체크박스 등의 컴포넌트 제작시 유리함  
- v-model이 돌아가는 구조를 통해 direct props mutations 방지  
- 동시에 상하위 컴포넌트 결합도 높아짐  
- datepicker, callendar, modal 등 세부적인 컴포넌트 작성시 유용한 테크닉  
4. renderless - 데이터 처리 컴포넌트  :  
- template 태그 없음  
- 데이터 처리 로직(axios 등)만 컴포넌트에 위임하고 화면 조작 로직만 부모 컴포넌트에서 처리하는 패턴
