<template>
  <div>
    <Row :gutter="20">
      <i-col span="24">
        <Table :columns="columns1" :data="data1"></Table>
      </i-col>
    </Row>
    <br>
    <Row :gutter="20">
      <i-col span="12">
        <Select v-model="model10" multiple style="width:260px">
          <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>
      </i-col>
      <i-col span="12">
        <DatePicker type="daterange" placement="bottom-end" placeholder="Select date" style="width: 200px"></DatePicker>
      </i-col>
    </Row>
    <br>
    <Row :gutter="20">
      <i-col span="12">
        <Card title="iview-admin交流群(已满)" shadow>
          <img class="qq-group-img" :src="qqFans" alt="">
          <p class="qq-group-intro">11本群为使用iview-admin或者对iview-admin感兴趣的开发者提供交流平台，在这里，解决你开发中的疑惑，共同进步。</p>
        </Card>
      </i-col>
      <i-col span="12">
        <Card title="iview-admin交流群2" shadow>
          <img class="qq-group-img" :src="qqFans2" alt="">
          <p class="qq-group-intro">本群为使用iview-admin或者对iview-admin感兴趣的开发者提供交流平台，在这里，解决你开发中的疑惑，共同进步。</p>
        </Card>
      </i-col>
    </Row>
  </div>
</template>

<script>
import qqFans from '@/assets/images/qq-group1.jpg'
import qqFans2 from '@/assets/images/qq-group2.jpg'
export default {
  name: 'my_page',
  data () {
    return {
      qqFans,
      qqFans2,
      cityList: [
        {
          value: 'New York',
          label: 'New York'
        },
        {
          value: 'London',
          label: 'London'
        },
        {
          value: 'Sydney',
          label: 'Sydney'
        },
        {
          value: 'Ottawa',
          label: 'Ottawa'
        },
        {
          value: 'Paris',
          label: 'Paris'
        },
        {
          value: 'Canberra',
          label: 'Canberra'
        }
      ],
      model10: [],
      columns1: [
        {
          title: 'Name',
          key: 'name'
        },
        {
          title: 'Age',
          key: 'age'
        },
        {
          title: 'Address',
          key: 'address'
        },
        {
          title: 'date',
          key: 'date'
        }
      ],
      data1: [
        {
          name: 'John Brown',
          age: 18,
          address: 'New York No. 1 Lake Park',
          date: '2016-10-03'
        },
        {
          name: 'Jim Green',
          age: 24,
          address: 'London No. 1 Lake Park',
          date: '2016-10-01'
        },
        {
          name: 'Joe Black',
          age: 30,
          address: 'Sydney No. 1 Lake Park',
          date: '2016-10-02'
        },
        {
          name: 'Jon Snow',
          age: 26,
          address: 'Ottawa No. 2 Lake Park',
          date: '2016-10-04'
        }
      ]
    }
  }
}
</script>

<style>
.qq-group-img{
  display: block;
  margin: 0 auto;
  width: 240px;
}
.qq-group-intro{
  padding: 20px;
  font-size: 16px;
}
</style>
