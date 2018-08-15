<template>
  <div class='md-layout md-gutter'>
      <ReadingItem v-for='item in items' :key='item.id' :link='item.value' :title='item.title' class="md-layout-item"/>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from "vue-property-decorator";
import ReadingItem from "@/components/ReadingItem.vue"; // @ is an alias to /src

@Component({
  components: {
    ReadingItem
  }
})
export default class ReadingList extends Vue {
  @Prop() private msg!: string;
  @Prop()
  private items = [
    {
      links: [
        { id: 1, title: "Blazor", value: "https://github.com/aspnet/Blazor" },
        {
          id: 2,
          title: "Steeltoe",
          value:
            "https://github.com/rwwilden/steeltoe-demo-worldfetch/tree/v0_1_blog"
        },
        { id: 3, title: "Steeltoe", value: "https://steeltoe.io/docs/" },
        {
          id: 4,
          title: "Steeltoe",
          value: "https://github.com/SteeltoeOSS/Samples/tree/master/Discovery"
        },
        {
          id: 5,
          title: "Steeltoe",
          value: "https://github.com/SteeltoeOSS/Samples/tree/master/MusicStore"
        },
        {
          id: 6,
          title: "Steeltoe",
          value: "https://github.com/SteeltoeOSS/Samples/blob/master/README.md"
        },
        { id: 7, title: "Steeltoe", value: "https://steeltoe.io/" },
        {
          id: 8,
          title: "Cloud Config",
          value: "https://cloud.spring.io/spring-cloud-config/"
        },
        {
          id: 9,
          title: "Cloud Config",
          value:
            "https://ronaldwildenberg.com/programming/steeltoe/2018/02/04/centralized-config-for-dotnet-core-with-spring-cloud-config-server.html"
        },
        {
          id: 10,
          title: "Observer c#",
          value: "https://github.com/christopherread/Obvs"
        },
        {
          id: 11,
          title: "Event bus",
          value:
            "https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/multi-container-microservice-net-applications/rabbitmq-event-bus-development-test-environment"
        },
        {
          id: 12,
          title: "Rx",
          value:
            "https://rehansaeed.com/reactive-extensions-part1-replacing-events/"
        },
        { id: 13, title: "Rx", value: "https://github.com/Microsoft/Tx" },
        {
          id: 14,
          title: "Tulin Bebek",
          value:
            "https://www.baby-walz.de/p/nuna-spielbuegel-fuer-babywippe-leaf-p1269898/?variantId=P1269898_100746558"
        },
        {
          id: 15,
          title: "Tulin Bebek",
          value:
            "https://vanbellebaby.nl/wipstoeltjes/1157-nuna-leaf-speelboog-voor-wipstoeltje-8717903888803.html"
        },
        {
          id: 16,
          title: "Tulin Bebek",
          value:
            "https://www.prenatal.nl/eten-en-drinken/kinderstoelen/wipstoelen/nuna-leaf-speelbeugel-102644.html"
        },
        {
          id: 17,
          title: "Tulin Bebek",
          value: "https://www.babypark.nl/nuna-leaf-speelbeugel-reversible.html"
        },
        { id: 18, title: "DDD", value: "https://github.com/ddd-cqrs-es" },
        {
          id: 19,
          title: "System Primer",
          value: "https://github.com/donnemartin/system-design-primer"
        },
        {
          id: 20,
          title: "Dotnet new nunit",
          value: "https://github.com/nunit/dotnet-new-nunit"
        },
        {
          id: 21,
          title: "Carter",
          value: "https://github.com/CarterCommunity/Carter"
        },
        {
          id: 22,
          title: "Dotnet templates",
          value:
            "https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new"
        },
        {
          id: 23,
          title: "16 Personalities",
          value: "https://www.16personalities.com/"
        },
        {
          id: 24,
          title: "Angry developer",
          value:
            "https://codeburst.io/why-developers-become-frustrated-and-companies-cant-find-talent-c4114d8b72ac"
        }
      ]
    }
  ];
}
</script>
