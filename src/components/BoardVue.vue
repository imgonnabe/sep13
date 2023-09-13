<template>
  <div class="board-back">
    <table>
        <tr>
            <td>번호</td>
            <td>제목</td>
            <td>글쓴이</td>
            <td>날짜</td>
            <td>읽음</td>
        </tr>
        <tr v-for="n in items" v-bind:key="n.boardNo"><!-- v-bind:key : 기준으로 나타난다. -->
            <td>{{n.boardNo}}</td>
            <td>{{n.title}}</td>
            <td>{{n.writer}}</td>
            <td>{{n.date}}</td>
            <td>{{n.read}}</td>
        </tr>
    </table>

    <div v-for="(n, index) in 10" v-bind:key="n">
        <div>{{n}} / {{index}}</div>
    </div>
    <br>
    <div v-for="n in 9" v-bind:key="n">
        <span v-for="i in 9" v-bind:key="i">
          {{n}} x {{i}} = {{i*n}}&nbsp;
        </span>
    </div>
  </div>
</template>

<script>
export default {
    data(){
      return{
        items : [
          {boardNo:10, title:'열번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:9, title:'아홉번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:8, title:'여덟번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:7, title:'일곱번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:6, title:'여섯번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:5, title:'다섯번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:4, title:'네번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:3, title:'세번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:2, title:'두번째 글', writer:'홍길동', date:'2023-09-13', read:150},
          {boardNo:1, title:'첫번째 글', writer:'홍길동', date:'2023-09-13', read:150},        
        ]
      }
    }
}
</script>

<style scoped>
  .board-back{
    height: 500px;
    width: 900px;
    margin: 0 auto;
    padding: 10px;
    background-color: gray;
  }
</style>