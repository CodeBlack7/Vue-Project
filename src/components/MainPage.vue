<template>
<div>
<h2 style="color: white;">Type the characters to count</h2>
<body class="main">
<div class="text">
<textarea style="white-space: pre-line;"  v-model="inputtext" placeholder="Type Here..."></textarea>
<h2 class="result"> 
  <a class="span5 teaser-container" href="https://loop.frontiers-ss-int.info/people/33924/overview" onclick="window.open('#','_blank');window.open(this.href,'_self');" >
        <article class="container-bordered">
            <div class="teaser author-info first" style="height: 133px">
                <div class="pull-left">
                    <img style="width: 55px; height: 55px" alt="" onerror="this.src='/Images/Frontiers/Common/Profile/default-profile-70.jpg'" data-default="/Images/Frontiers/Common/Profile/default-profile-70.jpg" src="https://loop.frontiers-ss-int.info/images/profile/33924/70">
                </div>

                <div class="teaser-text">
                    <h3 class="teaser-heading author-name" data-event="overviewtopiceditorname-link-click">
                        Sven Vanneste
                    </h3>
                    <p class="author-affiliation-name">
                        University of Texas at Dallas
                    </p>
                    <p class="author-affiliation-location">
                        Richardson, United States
                    </p>
                </div>
            </div>
            
        </article>
    </a>
Character Count : {{textcount}}
</h2>
</div>
</body>
</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class MainPage extends Vue {
  public inputtext :any = "";
 get textcount(){
   return this.inputtext.replace( /[\r\n]+/gm, "" ).length;
 }
 }
</script>
<style scoped lang="scss">
.result{
  color: white;
  padding-top: 10px;
}

.text{
 position: absolute;
    height: 85%;
    width: 98.5%;
}

textarea {
display: inline-block;
    margin: 0;
    padding: 5em;
    width: 90%;
    height: 80%;
    min-width: 30em;
    max-width: 100%;
    min-height: 10em;
    cursor: text;
    overflow: auto;
    resize: none;
    border: none;
    outline: none;
    font-size: 14px;
    font-weight: 300;
 
}
</style>
