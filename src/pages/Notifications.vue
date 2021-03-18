<template>
  <div class="row">
    <div class="col-md-6">
      <card>
        <h4 slot="header">Market News</h4>
        <base-alert type="info" dismissible>
          <span>EUR/USD goes down 10 pips</span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span>US Treasury Note goes up 50 pips</span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span>Premium for Tenor 1w remain the same, 0.0010%</span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span>Nom forecast EUR/USD trend down in next 1 week</span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span>Nom forecast JPY/USD trend up in next 2 week</span>
        </base-alert>
<!--        <base-alert type="info" dismissible with-icon>-->
<!--          <span data-notify="icon" class="tim-icons icon-bell-55"></span>-->
<!--          <span data-notify="message">This is a notification with close button and icon.</span>-->
<!--        </base-alert>-->
<!--        <base-alert type="info" dismissible with-icon>-->
<!--          <span data-notify="icon" class="tim-icons icon-bell-55"></span>-->
<!--          <span data-notify="message">This is a notification with close button and icon and have many lines. You can see that the icon and the close button are always vertically aligned. This is a beautiful notification. So you don't have to worry about the style.</span>-->
<!--        </base-alert>-->
      </card>
    </div>
    <div class="col-md-6">
      <card>
        <h4 slot="header">Client News</h4>
        <base-alert type="primary" dismissible>
          <span><b> BP102 - </b> New recommendation --- Premium received fir Tenor 1 month. </span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span><b> BP106 - </b> Client BP106 deposit 45,420.63 dollars in SGD.</span>
        </base-alert>
        <base-alert type="success" dismissible>
          <span><b> BP111 - </b> Client BP111 introduced Loan 422,527.80 JPY.</span>
        </base-alert>
        <base-alert type="warning" dismissible>
          <span><b> BP116 - </b> BP116 doesn't have Loan anymore. Not match the criteria to do FX Option.</span>
        </base-alert>
        <base-alert type="danger" dismissible>
          <span><b> BP115 - </b> BP115 doesn't have Loan anymore. Not match the criteria to do FX Option.</span>
        </base-alert>
      </card>
    </div>
<!--    <div class="col-md-12">-->
<!--      <card>-->
<!--        <div class="places-buttons">-->
<!--          <div class="row">-->
<!--            <div class="col-md-6 ml-auto mr-auto text-center">-->
<!--              <h4 class="card-title">-->
<!--                Notifications Places-->
<!--                <p class="category">Click to view notifications</p>-->
<!--              </h4>-->
<!--            </div>-->
<!--          </div>-->
<!--          <div class="row">-->
<!--            <div class="col-lg-8 ml-auto mr-auto">-->
<!--              <div class="row">-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('top', 'left')">Top Left</base-button>-->
<!--                </div>-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('top', 'center')">Top Center</base-button>-->
<!--                </div>-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('top', 'right')">Top Right</base-button>-->
<!--                </div>-->
<!--              </div>-->
<!--            </div>-->
<!--          </div>-->
<!--          <div class="row">-->
<!--            <div class="col-lg-8 ml-auto mr-auto">-->
<!--              <div class="row">-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('bottom', 'left')">Bottom Left</base-button>-->
<!--                </div>-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('bottom', 'center')">Bottom Center</base-button>-->
<!--                </div>-->
<!--                <div class="col-md-4">-->
<!--                  <base-button type="primary" block @click="notifyVue('bottom', 'right')">Bottom Right</base-button>-->
<!--                </div>-->
<!--              </div>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--      </card>-->
<!--    </div>-->
  </div>
</template>
<script>
  import NotificationTemplate from './Notifications/NotificationTemplate';
  import { BaseAlert } from '@/components';

  export default {
    components: {
      BaseAlert
    },
    data() {
      return {
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        }
      };
    },
    methods: {
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: NotificationTemplate,
          icon: "tim-icons icon-bell-55",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 0
        });
      }
    }
  };
</script>
<style>
</style>
