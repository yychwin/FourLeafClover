<template>
    <div class="row">
      <div class="col-12">
        <card :title="table1.title">
          <div class="table-responsive">
            <base-table :data="table1.data"
                        :columns="table1.columns"
                        thead-classes="text-primary">
            </base-table>
          </div>
        </card>
      </div>

<!--      <div class="col-12">-->
<!--        <card class="card-plain">-->
<!--          <div class="table-full-width table-responsive">-->
<!--            <base-table :title="table2.title" :sub-title="table2.subTitle" :data="table2.data"-->
<!--                         :columns="table2.columns">-->

<!--            </base-table>-->
<!--          </div>-->
<!--        </card>-->
<!--      </div>-->

    </div>
</template>
<script>
import { BaseTable } from "@/components";
const tableColumns = ["BPNumber", "Name","Type", "CCY", "Amount","Spot","Strike","FX Option Available"];
const tableData = [
    {
        "id": 1,
        "bpnumber": "102",
        "name":"William",
        "amount": "243,711.07",
        "type": "Loan",
        "ccy": "EUR",
        "spot":"",
        "strike":"",
        "fx option available":"Yes"
    },
    {
        "id": 2,
        "bpnumber": "",
        "amount": "1,087,060.58",
        "type": "Cash",
        "ccy": "USD",
        "spot":"1.1950",
        "strike":"1.1850",
        "fx option available":""
    },
    {
        "id": 3,
        "bpnumber": "",
        "amount": "3,007,874.13",
        "type": "Cash",
        "ccy": "JPY",
        "spot":"130.2000",
        "strike":"129.2000",
        "fx option available":""
    },
    {
        "id": 4,
        "bpnumber": "106",
        "name":"James",
        "amount": "422,527.80",
        "type": "Loan",
        "ccy": "JPY",
        "spot":"",
        "strike":"",
        "fx option available":"Yes"
    },
    {
        "id": 5,
        "bpnumber": "",
        "amount": "45,420.63",
        "type": "Cash",
        "ccy": "SGD",
        "spot":"81.0000",
        "strike":"82.0000",
        "fx option available":""
    },
    {
        "id": 6,
        "bpnumber": "111",
        "name":"Mason",
        "amount": "281,861.74",
        "type": "Loan",
        "ccy": "EUR",
        "spot":"",
        "strike":"",
        "fx option available":"Yes"
    },
    {
        "id": 7,
        "bpnumber": "",
        "amount": "1,480,355.14",
        "type": "Cash",
        "ccy": "JPY",
        "spot":"130.2000",
        "strike":"129.2000",
        "fx option available":""
    },
    {
        "id": 8,
        "bpnumber": "116",
        "name":"Ella",
        "amount": "396,300.70",
        "type": "Cash",
        "ccy": "AUD",
        "spot":"",
        "strike":"",
        "fx option available":"No"
    },
    {
        "id": 9,
        "bpnumber": "",
        "amount": "1,150,210.37",
        "type": "Cash",
        "ccy": "JPY",
        "spot":"130.2000",
        "strike":"129.2000",
        "fx option available":""
    },
    {
        "id": 10,
        "bpnumber": "",
        "amount": "51,982.05",
        "type": "Cash",
        "ccy": "SGD",
        "spot":"",
        "strike":"",
        "fx option available":""
    },
    {
        "id": 11,
        "bpnumber": "115",
        "name":"Jackson",
        "amount": "341,487.20",
        "type": "Cash",
        "ccy": "HKD",
        "spot":"",
        "strike":"",
        "fx option available":"No"
    },
    {
        "id": 11,
        "bpnumber": "",
        "name":"",
        "amount": "76,543.90",
        "type": "Cash",
        "ccy": "USD",
        "spot":"",
        "strike":"",
        "fx option available":""
    },
    {
        "id": 11,
        "bpnumber": "",
        "name":"",
        "amount": "333,889,124.35",
        "type": "Cash",
        "ccy": "JPY",
        "spot":"",
        "strike":"",
        "fx option available":""
    }
];

export default {
  components: {
    BaseTable
  },
  data() {
    return {
      table1: {
        title: "Client Assets",
        columns: [...tableColumns],
        data: [...tableData]
      },
      table2: {
        title: "Table on Plain Background",
        columns: [...tableColumns],
        data: [...tableData]
      }
    };
  }
};
</script>
<style>
</style>
