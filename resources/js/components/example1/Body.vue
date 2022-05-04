<template>
    <div class="body">
        <!-- 텍스트의 색깔 -->
        <span>span</span>

        <!-- 사각형을 그리는데, BG COLOR 다름, 테두리 색, 테두리 둥글게 표시 -->
        <div>div</div>

        <!-- A 태그 naver.com 연결 // 누르면 보라색으로 바뀜. 안바뀌게. -->
        <a>anchor</a>

        <!-- 폰트 값을 Arial, 사이즈도 바꾸고, 밑줄을 칩니다 -->
        <p>p</p>

        <!-- 커서를 갖다대면 손가락이 나옴 -->
        <h1>h1</h1>
    </div>
</template>

<script>
export default {
    name: "Body"
}
</script>

<style>
    .body { flex-grow: 1; background: #fafafa; }
</style>
