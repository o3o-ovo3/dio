<template>
  <div class="mycont-box" id="container">
    <div class="mycalling-plan">
      <h4 class="name">이용중인 요금제</h4>
      <p class="plan">
        {{ moUseProdInfoDto.vasProdNm }}
         <!--티빙/지니/밀리 초이스-->
      </p>
    </div>
    <div class="calling-planbox">
      <div class="calling-head">
        <div class="flat-rate-pricing">
          <strong class="name">월 실납부금액 <span class="intext">(부가세포함)</span></strong          >
          <strong class="price">{{ moUseProdInfoDto.realProdSaleAmtVat }}</strong
          >
        </div>
        <p class="calling-change">
          <strong class="text">변경일</strong>
          {{ moUseProdInfoDto.efctStDt }}
        </p>
      </div>
      <div class="calling-plan-box">
        <table class="calling-plan-data">
          <caption>
            데이터, 음성, 문자의 순서로 이용중인 요금제에 대한 정보표
          </caption>
          <colgroup>
            <col style="width: 9%" />
            <col style="width: 61%" />
            <col style="width: 8%" />
            <col style="width: 22%" />
          </colgroup>
          <tbody>
            <tr>
              <th scope="row">데이터</th>
              <td colspan="3">
                {{ moUseProdInfoDto.prodDataSbst }}
              </td>
            </tr>
            <tr>
              <th scope="row">음성</th>
              <td>
                {{ moUseProdInfoDto.prodVcSbst }}
              </td>
              <th scope="row">문자</th>
              <td>{{ moUseProdInfoDto.prodChrSbst }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <ul class="list-dot">
      <!--
      <li v-if="isYogoPrice === 'ALL'">프로모션 기간 내 요금제를 최초/변경 가입하신 경우, 추가 데이터 및 멤버십 VIP 요금제 혜택이 제공됩니다. <a href="#" @click="trackClick('KT-개인_마이', 'KT-개인_마이_요금/서비스', '내모바일요금제', '프로모션자세히보기')"><strong>프로모션 자세히 보기</strong></a></li>
      <li v-if="isYogoPrice === 'VIP'">프로모션 기간 내 요금제를 최초/변경 가입하신 경우, 멤버십 VIP 요금제 혜택이 제공됩니다. <a href="#" @click="trackClick('KT-개인_마이', 'KT-개인_마이_요금/서비스', '내모바일요금제', '프로모션자세히보기')"><strong>프로모션 자세히 보기</strong></a></li>
      <li v-if="isYogoPrice === 'DATA'">프로모션 기간 내 요금제를 최초/변경 가입하신 경우, 추가 데이터 혜택이 제공됩니다. <a href="#" @click="trackClick('KT-개인_마이', 'KT-개인_마이_요금/서비스', '내모바일요금제', '프로모션자세히보기')"><strong>프로모션 자세히 보기</strong></a></li>
      <li v-if="isRealPayPriceOpen && moUseProdInfoDto.realProdSaleAmtVat !== null && moUseProdInfoDto.realProdSaleAmtVat !== ''">
      -->
      <li>
        실납부금액은
        <strong class="pointer">결합/요금/복지할인 등이 반영된 금액</strong
        >이며, 실제 청구되는 금액과는 차이가 있을 수 있습니다.
      </li>
      <li>
        요금제 변경/예약 혹은 옵션 설정은 ‘마이 &gt; 요금/서비스 &gt;
        <a :href="`/product/MobilePriceView.do`" class="decoration pointer"
          >요금제 변경</a
        >’ 에서 가능합니다.
      </li>
    </ul>
  </div>
</template>

<script>
import './assets/css/global.css';
export default {
  data() {
    return {
      moUseProdInfoDto: {
        vasProdNm: "티빙/지니/밀리 초이스 베이직_Y덤", // Add actual data
        
        realProdSaleAmtVat: "90,000원", // Add actual data
        //prodSaleAmtVat: "", // Add actual data
        efctStDt: "2024.07.30", // Add actual data
        prodDataSbst: "완전 무제한 (스마트기기/테더링 데이터 80GB)", // Add actual data
        prodVcSbst: "무제한 (영상/부가 300분)", // Add actual data
        prodChrSbst: "기본제공" // Add actual data
      }/*,
      isYogoPrice: "", // 'ALL', 'VIP', 'DATA' etc.
      prodSaleAmtEtcYN: "", // 'Y' or 'N'
      */
    }
  }/*,
  computed: {
    isRealPayPriceOpen() {
      return this.openDateChkYn('REALPAYPRICE_SHOW_OPEN'); // Your implementation
    }
  },
  methods: {
    trackClick(category, action, label, value) {
      // Implement your tracking logic here
      console.log(`Tracking click: ${category}, ${action}, ${label}, ${value}`);
    },
    openDateChkYn(param) {
      // Your logic to check date
      return true; // Placeholder
    }*/
  }
</script>
<!--
<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Hello Vue World"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

-->
