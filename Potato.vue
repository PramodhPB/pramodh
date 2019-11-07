<template>
  <div style="margin-top:10px;">
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" class="img1">
          <p>
            <u>This is a page for potato voting</u>
          </p>
        </b-col>
        <b-col sm="6" class="img">
          <p>Made By With Love By [Name]</p>
        </b-col>
      </b-row>
    </b-container>
    <!-- <b-container class="bv-example-row"> -->

    <b-container class="cart-bg">
      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img src="./mashedPotato.jpg" width="150" height="90" />
            </b-nav-item>
            <b-nav-item>
              <b-button @click="likes+=1;" class="demo">likes</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <p class="para demo">
                likes:
                <span class="ans">{{likes}}</span>
              </p>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img
                src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/bakedPotato.jpeg"
                width="150"
                height="90"
              />
            </b-nav-item>
            <b-nav-item>
              <b-button @click="dislikes+=1" class="dislikebtn demo">Dislikes</b-button>
            </b-nav-item>
            <b-nav-item>
              <p class="demo">Dislikes:{{dislikes}}</p>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="6" offset="5" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <b-button @click="restbtn" class="resetbtn">Reset</b-button>
            </b-nav-item>
            <b-nav-item>
              <p class="para">
                Total clicks:
                <span class="ans">{{likes+dislikes}}</span>
              </p>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>

      <br />
    </b-container>
    
  </div>
</template>
<script>
export default {
  name: "potato",

  data() {
    return {
      likes: 0,
      dislikes: 0
    };
  },
  methods: {
    restbtn() {
      this.likes = 0,
       this.dislikes = 0;
      // this.total='0'
    }
  }
};
</script>
<style scoped>
.ans {
  color: #f1f943;
  font-size: 30px;
}
p {
  font-size: 25px;
  color: #fff;
}
.para {
  color: aliceblue;
}
.middle-part {
  width: 50%;
  margin: 0 auto;
  position: absolute;
  top: 50px;
  left: 250px;
}

.img1 {
  background-image: url(../potato/blue.png);
  height: 30vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.img1 p {
  font-size: 40px;
  position: absolute;
  top: 50px;
  left: 50px;
  color: black;
}
.img {
  background-image: url(../potato/thumbs.png);
  height: 30vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.img p {
  font-size: 40px;
  position: absolute;
  top: 50px;
  left: 50px;
  color: black;
}
.cart-bg {
  background-image: url(../potato/black.png);
  height: auto;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  /* position: relative; */
}
.img-btn {
  display: flex;
}
.potato-banner {
  padding: 20px;
}
.dislikebtn {
  background-color: red;
  /* margin-top: 20px; */
}
.resetbtn {
  background-color: #f1f943;
  color: black;
}
</style>
