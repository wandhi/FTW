<template>
  <card class="card-stats" :show-footer-line="true">
    <b-row>

      <b-col style="display:flex;justify-content:center;align-items:center;flex-direction:column;height:98px">
        <slot>
          <span :style="{color:[color]+'!important','font-size':'24px','font-weight':600}" class="card-title  text-muted mb-0" v-if="title ||!color">{{title}}</span>
          <span style="font-size:12px;font-weight:normal;line-height:10.02px;margin-top:15px" class="h2  mb-0" v-if="subTitle"><span v-if="label" :style="{color:[labelColor]+'!important'}">{{label}}</span> {{subTitle}}</span>
          <span v-if="bottomText" style="font-size:12px;margin-top:15px">{{bottomText}}</span>
        </slot>
      </b-col>

      <b-col cols="auto" v-if="$slots.icon || icon">
        <slot name="icon">
          <div class="icon icon-shape text-white rounded-circle shadow"
               :class="[`bg-${type}`, iconClasses]">
            <i :class="icon"></i>
          </div>
        </slot>
      </b-col>
    </b-row>

    <p class="mt-3 mb-0 text-sm">
      <slot name="footer">

      </slot>
    </p>
  </card>
</template>
<script>
  import Card from './Card.vue';

  export default {
    name: 'stats-card',
    components: {
      Card
    },
    props: {
      type: {
        type: String,
        default: 'primary'
      },
      icon: String,
      title: String,
      subTitle: String,
      iconClasses: [String, Array],
      color:String,
      label:String,
      labelColor:String,
      bottomText:String
    }
  };
</script>
<style></style>
