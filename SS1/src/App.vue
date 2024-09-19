<script setup>
import Card from './components/card.vue'
</script>

<template>
  <div>
    <div>
      <h1>Bai 1</h1>
      <h3>Danh sach khoa hoc</h3>
      <p>1. Html <br> 2. Css <br> 3. Javascript <br> 4. ReactJs</p>
    </div>

    <div>
      <h1>Bai 2</h1>
      <div class="box-container">
        <div class="a">1</div>
        <div class="b">2</div>
        <div class="c">3</div>
      </div>
    </div>

    <div>
      <h1>Bai 3</h1>
      <Card></Card>
    </div>
    <div>
      <h1>Bai 4</h1>
      <h3>a-b ={{c[0]}}</h3>
      <h3>a+b ={{c[1]}}</h3>
      <h3>a*b ={{c[2]}}</h3>
      <h3>a/b ={{c[3]}}</h3>
    </div>
    <div>
      <h1>Bai 5</h1>
      <h3>name :{{d.name}}</h3>
      <h3>sex :{{d.sex}}</h3>
      <h3>date :{{d.date}}</h3>
      <h3>email :{{d.email}}</h3>
      <h3>address :{{d.address}}</h3>
    </div>
    <div>
      <h1>Bai 6</h1>
      <h3>{{format(user.a , user.b)}}</h3>
    </div>
    <div>
      <h1>Bai 7</h1>
      <div class="e">navbar</div>
      <div class="h">
        <div class="f">menu</div>
        <div>
          <div class="g">hihi</div>
          <div class="w">huhu</div>
        </div>
      </div>
    </div>
    <div>
      <h1>Bai 9</h1>
      <table>
        <tr>
          <th>Stt</th>
          <th>Name</th>
          <th>Date</th>
          <th>Sex</th>
          <th>Address</th>
          <th>Action</th>
        </tr>
        <tr v-for="(item,index) in ab" :key="index">
           <td>{{ item.name }}</td>
           <td>{{ item.sex }}</td>
           <td>{{ item.date }}</td>
           <td>{{ item.email }}</td>
           <td>{{ item.address }}</td>
           <td>
            <button class="s">Sua</button>
            <button class="x">Xoa</button>
           </td>
         
        </tr>
      </table>
    </div>
    <div>
      <div class="card-body p-5">
              <Header />
              <TaskForm />
              <TodoList />
            </div>
    </div>
  </div>
</template>

<style scoped>
.a, .b, .c {
  width: 200px;
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 24px;
}

.a {
  background-color: red;
}

.b {
  background-color: blue;
}

.c {
  background-color: yellow;
}

.box-container {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.e{
  justify-content: center;
  text-align: center;
  background-color: gray;
  width:1000px;
  height: 40px;
}
.f{
  justify-content: center;
  text-align: center;
  background-color: blue;
  width:300px;
  height: 500px;
}
.g{
  justify-content: center;
  text-align: center;
  background-color: rgb(201, 237, 20);
  width:700px;
  height: 460px;

}
.h{
  display: flex;
  flex-direction: row;

}
.w{
  justify-content: center;
  text-align: center;
  background-color: gray;
  width:700px;
  height: 40px;
}
.x{
  width:50px ;
  height: 30px;
  background-color: red;
  color: white;
}
.s{
  width:50px ;  
  height: 30px;
  background-color: white;
  color: black;
}
</style>
<script>
const a = 10
const b = 10;
const c= [(a-b),(a+b),(a*b),(a/b)]
const d ={
  name:'A',
  sex:'nam',
  date:'1/2/2003',
  email:'a@gmail.com',
  address:"ha noi"
}
const user ={
  a:'bui duy',
  b:'anh'
}
const format=(a,b)=>{
  return a+" "+b
}
const ab =[
  {
    name:'A',
  sex:'nam',
  date:'1/2/2003',
  email:'a@gmail.com',
  address:"ha noi"
  },
  {
    name:'B',
  sex:'nu',
  date:'1/2/2004',
  email:'b@gmail.com',
  address:"ha noi"
  }

]
</script>
