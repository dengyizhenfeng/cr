<template>
  <view class="index">
    <AtNoticebar marquee>
      如不是通过搜索"千成林"小程序使用的可能为体验版，体验版不稳定，可搜索"千成林"使用正式版
    </AtNoticebar>
    <AtSegmentedControl
      :on-click="handleClick"
      :current="current1"
      :values="tabList2"
    />
    <AtForm>
      <view
        v-show="current1 === 0"
        class="tab-content"
      >
        <view class="item">
          <text class="tip">
            传奇换币卡
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/chuanqibi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.bi1"
              :on-change="val => handleNumberChange('bi1', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            史诗换币卡
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/shishibi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.bi2"
              :on-change="val => handleNumberChange('bi2', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            稀有换币卡
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/xiyoubi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.bi3"
              :on-change="val => handleNumberChange('bi3', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            普通换币卡
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/putongbi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.bi4"
              :on-change="val => handleNumberChange('bi4', val)"
            />
          </view>
        </view>
      </view>
      <view
        v-show="current1 === 1"
        class="tab-content"
      >
        <view class="item">
          <text class="tip">
            黄金宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/huangjin.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.hj"
              :on-change="val => handleNumberChange('hj', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            巨型宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/juxing.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.jx"
              :on-change="val => handleNumberChange('jx', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            神奇宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/shenqi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.sq"
              :on-change="val => handleNumberChange('sq', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            史诗宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/shishi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.ss"
              :on-change="val => handleNumberChange('ss', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            传奇宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/chuanqi.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.cq"
              :on-change="val => handleNumberChange('cq', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            雷电宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/ld.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.ld"
              :on-change="val => handleNumberChange('ld', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            超级雷电宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/chaolei.png')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.cl"
              :on-change="val => handleNumberChange('cl', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            传奇国王宝箱
          </text>
          <view class="content">
            <image
              class="img"
              :src="require('@/assets/cqgw.jpg')"
              mode="widthFix"
            />

            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.cg"
              :on-change="val => handleNumberChange('cg', val)"
            />
          </view>
        </view>
      </view>
      <view
        v-show="current1 === 2"
        class="tab-content"
      >
        <view class="item">
          <text class="tip">
            表情个数
          </text>
          <view class="content">
            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.biaoqing"
              :on-change="val => handleNumberChange('biaoqing', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            金币个数
          </text>
          <view class="content">
            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.jinbi"
              :on-change="val => handleNumberChange('jinbi', val)"
            />
          </view>
        </view>
        <view class="item">
          <text class="tip">
            宝石个数
          </text>
          <view class="content">
            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="form.baoshi"
              :on-change="val => handleNumberChange('baoshi', val)"
            />
          </view>
        </view>
      </view>
      <view
        v-show="current1 === 3"
        class="tab-content"
      >
        <view class="item">
          <text class="tip">
            人命币
          </text>
          <view class="content">
            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="jia.jiage1"
              :on-change="val => handleChange('jiage1', val)"
            />
          </view>
        </view>

        <view class="item">
          <text class="tip">
            宝石
          </text>
          <view class="content">
            <AtInputNumber
              :width="200"
              :min="0"
              :max="99999999"
              :step="1"
              :value="jia.jiage2"
              :on-change="val => handleChange('jiage2', val)"
            />
          </view>
        </view>
      </view>
    </AtForm>
    <text class="result">
      {{ xingjiabi }}
    </text>

    <view class="caozuo">
      <AtButton
        type="primary"
        :on-click="onSubmit"
      >
        查询
      </AtButton>
      <AtButton
        type="secondary"
        :on-click="reset"
      >
        重置
      </AtButton>
    </view>
    <view class="shuoming">
      <text class="shuomingtip">
        百分比说明：
      </text>
      <AtList>
        <AtListItem
          note="血🐴赚"
          title="110%以上"
        />
        <AtListItem
          note="血赚"
          title="100%~110%"
        />
        <AtListItem
          note="可以买"
          title="90%~99%"
        />
        <AtListItem
          note="小亏"
          title="80%-90%"
        />
        <AtListItem
          note="亏"
          title="70%-80%"
        />
        <AtListItem
          note="血亏"
          title="60%-70%"
        />
        <AtListItem
          note="血🐴亏"
          title="低于60%"
        />
      </AtList>
    </view>
  </view>
</template>

<script>
import { AtInputNumber, AtSegmentedControl, AtForm, AtInput, AtButton, AtMessage, AtList, AtListItem, AtNoticebar } from 'taro-ui-vue'
import Taro from '@tarojs/taro'
import 'taro-ui-vue/dist/style/components/input-number.scss'
import 'taro-ui-vue/dist/style/components/segmented-control.scss'
import 'taro-ui-vue/dist/style/components/flex.scss'
import 'taro-ui-vue/dist/style/components/form.scss'
import 'taro-ui-vue/dist/style/components/input.scss'
import 'taro-ui-vue/dist/style/components/icon.scss'
import 'taro-ui-vue/dist/style/components/button.scss'
import 'taro-ui-vue/dist/style/components/message.scss'
import 'taro-ui-vue/dist/style/components/list.scss'
import 'taro-ui-vue/dist/style/components/noticebar.scss'
import './index.scss'

export default {
  name: 'Index',
  components: {
    AtSegmentedControl,
    AtForm,
    AtInputNumber,
    AtButton,
    AtList,
    AtListItem,
    AtNoticebar,
  },
  data() {
    return {
      jia: {
        jiage1: '',
        jiage2: '',
      },
      current1: 0,
      tabList2: ['换币卡', '宝箱', '金币宝石等', '宝箱价格'],
      xingjiabi: '',
      jiage: '',
      form: {
        bi1: 0,
        bi2: 0,
        bi3: 0,
        bi4: 0,
        hj: 0,
        jx: 0,
        sq: 0,
        ss: 0,
        cq: 0,
        cl: 0,
        cg: 0,
        ld: 0,
        biaoqing: 0,
        baoshi: '',
        jinbi: '',
      },
      prices: {
        bi1: 20000,
        bi2: 5000,
        bi3: 2500,
        bi4: 1250,
        ld: 3444.95,
        hj: 1408.12,
        jx: 8331.2,
        sq: 11344.5,
        ss: 10000,
        cq: 20000,
        cl: 53412,
        cg: 41215,
      },
    }
  },
  methods: {
    handleClick(value) {
      this.current1 = value
    },
    handleChange(prop, val) {
      this.jia[prop] = val
    },
    handleNumberChange(prop, val) {
      this.form[prop] = val
    },
    onSubmit() {
      if (!this.jia.jiage1 && !this.jia.jiage2) {
        Taro.showToast({
          title: '请先填入宝箱价格！',
          icon: 'none',
        })
        return
      }
      if (this.jia.jiage1 && this.jia.jiage2) {
        Taro.showToast({
          title: '价格只可输入一项，不可同时输入！',
          icon: 'none',
        })
        return
      }
      let xujia = 0
      Object.keys(this.prices).forEach((k) => {
        xujia = xujia + Number(this.form[k]) * Number(this.prices[k])
      })
      xujia = xujia + Number(this.form.jinbi) * 1.2
      let xujiajiagewu = (xujia / 10000) * 3
      if (this.form.biaoqing) xujiajiagewu = xujiajiagewu + 6
      if (this.form.baoshi) xujiajiagewu = xujiajiagewu + (Number(this.form.baoshi) / 500) * 25
      const rmb = this.jia.jiage1 || (Number(this.jia.jiage2) / 500) * 25
      console.log('rmb', rmb)
      this.xingjiabi = Math.round((xujiajiagewu / rmb) * 10000) / 100 + '%'
    },
    reset() {
      this.form = {
        bi1: 0,
        bi2: 0,
        bi3: 0,
        bi4: 0,
        hj: 0,
        jx: 0,
        sq: 0,
        ss: 0,
        cq: 0,
        cl: 0,
        cg: 0,
        ld: 0,
        biaoqing: 0,
        baoshi: '',
        jinbi: '',
      }
      this.form.baoshi = ''
      this.form.jinbi = ''
      this.jia.jiage1 = ''
      this.jia.jiage2 = ''
      this.xingjiabi = ''
    },
  },
  onHide() {
    this.reset()
  }
}
</script>
