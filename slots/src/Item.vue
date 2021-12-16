<template>
  <li>
    <h3>
      <slot name="title">
        <!-- NOTE: 등록하는 곳에서 정의할 화면 영역 -->
      </slot>
    </h3>
    <hr />
    <slot name="content"></slot>
  </li>
</template>
