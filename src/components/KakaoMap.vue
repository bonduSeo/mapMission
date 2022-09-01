<template>
  <div>
    <div id="map" style="width: 500px; height: 400px"></div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      sampleData: "",
    };
  },
  setup() {},
  created() {},
  mounted() {
    if (!window.kakao || !window.kakao.maps) {
      const script = document.createElement("script");
      script.src = "//dapi.kakao.com/v2/maps/sdk.js?autoload=false&appkey=a5184c558178073060039d181ee642d2";
      document.head.appendChild(script);

      script.addEventListener("load", () => {
        console.log("loaded", window.kakao);
      });
    } else {
      console.log("이미 로딩 됨:", window.kakao);
    }
  },
  unmounted() {},
  methods: {
    // drawMap() {
    //   var container = document.getElementById("map"); //지도를 담을 영역의 DOM 레퍼런스
    //   var options = {
    //     //지도를 생성할 때 필요한 기본 옵션
    //     center: new kakao.maps.LatLng(33.450701, 126.570667), //지도의 중심좌표.
    //     level: 3, //지도의 레벨(확대, 축소 정도)
    //   };
    //   var map = new kakao.maps.Map(container, options); //지도 생성 및 객체 리턴
    // },
  },
};
</script>
