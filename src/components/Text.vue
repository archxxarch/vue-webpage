<template>
    <section id="textType" class="text__wrap" :class="element">
        <span>{{ title }}</span>
        <h2>스크립트를 익히는 방법</h2>
        <div class="text__inner container">
            <div :class="'text t' + (key + 1)" v-for="(text, key) in textInfo" :key="key">
                <h3 class="text__title">{{ text.title }}</h3>
                <p class="text__desc">{{ text.desc }}</p>
                <a class="text__btn" href={text.src}>더보기</a>
            </div>

        </div>
    </section>
</template>

<script>
export default {
    props: {
        element: String,
        title: String
    },
    data: function () {
        return {
            textInfo: [
                {
                    title: "검색 이펙트",
                    desc: "자바스크립트의 기본 메서드를 통해 검색 스크립트를 완성하는 튜토리얼입니다. 메서드를 통해 쉽게 검색을 만들 수 있습니다.",
                    src: "/"
                },
                {
                    title: "퀴즈 이펙트",
                    desc: "주관식 및 객관식 퀴즈를 통해 데이터를 주고 받는 방법에 대해서 익히는 튜토리얼입니다.",
                    src: "/"
                },
                {
                    title: "마우스 이펙트",
                    desc: "마우스를 통해 요소를 움직이고 효과를 주는 스크립트 튜토리얼입니다. 다양한 효과를 통해 스크립트를 익힐 수 있습니다.",
                    src: "/"
                },
                {
                    title: "슬라이드 이펙트",
                    desc: "플러그인을 사용하지 않고 이미지 슬라이드를 표현하는 방법에 대해서 체계적으로 배우는 스크립트입니다.",
                    src: "/"
                },
                {
                    title: "패랠랙스 이펙트",
                    desc: "패랠랙스 스크로링 사이트에서 많이 사용되는 기법을 자바스크립트를 통해 익힙니다. 실무에서 가장 많이 쓰이는 스크립트입니다.",
                    src: "/"
                },
                {
                    title: "게임 이펙트",
                    desc: "게임을 통해 자바스크립트를 익힙니다. 어려울 수 있지만 하다보면 재밌는 게임 만들기 스크립트입니다.",
                    src: "/"
                },
            ]
        }
    }
}
</script>