<template>
    <div>
    <md-card md-with-hover>
      <md-ripple>
        <md-card-header>
          <div class="md-title">{{title}}</div>
        </md-card-header>

        <md-card-content>
          {{link}}
        </md-card-content>

        <md-card-actions>
          <md-button :href='link' target='blank'>Go to detail</md-button>
        </md-card-actions>
      </md-ripple>
    </md-card>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class ReadingItem extends Vue {
  @Prop() public link!: string;
  @Prop() public title!: string;
}
</script>
