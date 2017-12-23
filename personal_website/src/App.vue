<template>
  <div id="app">
    <div class = "home-section">
      <div class = "introduction">
        <h1 class = "name"> Yuh-Chian, Wu </h1>
        <h3 class = "introduce"> hello, haahahahaaha </h3>
      </div>
    </div>
    <div class = "whitebg-section">
      <div class = "section-content">
        <div class = "title">
          <h1> About </h1>
          <img src = "static/user.png" width="60px">
        </div>
        <div class = "content">
          <h2>Yuh-Chian, Wu</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Lectus arcu bibendum at varius. Amet tellus cras adipiscing enim eu turpis egestas. Orci porta non pulvinar neque laoreet suspendisse interdum consectetur. Nibh praesent tristique magna sit.</p>
        </div>
      </div>
    </div>
    <div class = "bluebg-section">
      <div class = "section-content">
        <div class = "title">
          <h1> Education </h1>
          <img src = "static/mortarboard.png" width="60px">
        </div>
        <div class = "content">
          <div class = "box" v-for="item in eduaction">
            <h2> {{item.school}} </h2>
            <div class = "small">Sept. 2016 - Present</div>
            <p> Master Degree </p>
          </div>
        </div>
      </div>
    </div>
    <div class = "whitebg-section">
      <div class = "section-content">
        <div class = "title">
          <h1>Skills</h1>
          <img src = "static/skills.png" width="60px">
        </div>
        <div class = "content">
          <div class = "box" v-for="item in skills">
            <img :src = "item.image" width="20px">
            <h2> {{item.skill_name}} </h2>
            <div class = "small"></div>
            <p> {{item.skills}} </p>
          </div>
        </div>
      </div>
    </div>
    <div class = "bluebg-section">
      <div class = "section-content">
        <div class = "title">
          <h1>Publication</h1>
          <img src="static//publication.png" width="60px">
        </div>
        <div class = "content">
          <div>
            <div class = "projectbox" v-for="item in publication">
              <img :src="item.image" width = "100%">
              <h3> {{item.title}} </h3>
              <div class = "small">CHI'17</div>
              <div class = "tag" v-for = "tech in item.tech"> {{tech}} </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data () {
    return {
      eduaction: [
        {
          school: 'National Taiwan University',
        },
        {
          school: 'National Taipei University',
        }
      ],
      skills:[
        { 
          image: 'static/file-code.png',
          skill_name: 'Programming Languages',
          skills: 'C/C++, Python, JavaScript, C#'
        },
        {
          image: 'static/grid-world.png',
          skill_name: 'Web-related',
          skills: 'PHP, HTML(pug), CSS(sass), Vue.js, Node.js'
        },
        {
          image: 'static/settings.png',
          skill_name: 'Tools',
          skills: 'Unity3D, Arduino, QT, Raspberry pi'
        },
      ],
      publication: [
        {
          image: 'static/ActiveErgo.png',
          title: 'ActiveErgo: Automatic and Personalized Ergonomicsusing Self-actuating Furniture',
          tech: ['Untiy', 'C#', 'Arduino']
        },
        {
          image: 'static/Peritext.png',
          title: 'PeriText: Utilizing Peripheral Vision for Reading Text onAugmented Reality Smart Glasses',
          tech: ['Untiy', 'C#', 'HTML', 'JavaScript', 'Microsoft Hololens']
        },
        {
          image: 'static/ActiveErgo.png',
          title: 'ActiveErgo: Automatic and Personalized Ergonomicsusing Self-actuating Furniture',
          tech: ['Untiy', 'C#', 'Arduino']
        },
        {
          image: 'static/ActiveErgo.png',
          title: 'ActiveErgo: Automatic and Personalized Ergonomicsusing Self-actuating Furniture',
          tech: ['Untiy', 'C#', 'Arduino']
        },
        {
          image: 'static//ActiveErgo.png',
          title: 'ActiveErgo: Automatic and Personalized Ergonomicsusing Self-actuating Furniture',
          tech: ['Untiy', 'C#', 'Arduino']
        }
      ]
    }
  }
}
</script>

<style lang="sass">
@media screen and (max-width: 768px)
  .is-not-mobile
    display: none
  .section-content
    flex-direction: column 
    .title
      margin-bottom: 16px
      padding: 0px 5px
    .content
      padding: 0px 0px
@media screen and (min-width: 769px)
  .is-not-mobile
    display: inherit
.projectbox
  padding: 0 10px
  width: 45%
  height: 400px
  float: left
  img
    width: 90%
    border: 1px solid #eee
    border-radius: 10px
    margin-bottom: 10px
    cursor: pointer
  .small
    color: #deeef5
  h3
    font-size: 15px
    color: white
    text-transform: none
    font-weight: normal
    margin: 5px 0
html,body 
 margin: 0
 height: 100%
 font-family: Arial, "Helvetica Neue", Helvetica, sans-serif
.home-section
  display: table
  height: 700px
  width: 100%
  position: relative
  background: linear-gradient(to bottom, rgba(34,125,170,1) 0%, rgba(81,172,205,1) 100%)
  .introduction 
    vertical-align: middle
    display: table-cell
    padding: 10px 100px
    .name
      font-size: 5em
      color: white
      margin: 0
    .introduce
      color: white
.whitebg-section
  display: block
  .title
    h1
      color: #3295be
      &::after
        border: 2px solid #3295be
.title
  width: 20%
  float: left
  h1
    margin-top: 0px
    margin-bottom: 16px
    &::after
      content: ' '
      display: block
      width: 50px
      margin: 10px 0
  img
    margin: 0 auto
.content
  float: left
  padding: 0px 50px
  width: 80%
  display: block
  h2
    color: #58798c
  p
    margin: 0
    color: #58798c
    font-size: 18px
    line-height: 30px
.section-content
  padding: 100px 100px
  display: flex
.small
  font-size: 14px
  color: #aac7d9
  margin-bottom: 5px
.box
  border: 1px solid #89bbd3
  border-radius: 10px
  padding: 20px
  color: white
  margin-bottom: 20px
  transition: all ease 0.5s
  h2
    display: inline
.bluebg-section
  background: linear-gradient(to bottom, rgba(34,125,170,1) 0%, rgba(81,172,205,1) 100%)
  .title
    h1
      color: white
      &::after
        border: 2px solid white
  h2
    color: white
    text-transform: none
.tag
  border: 1px solid #ddd
  display: inline-block
  border-radius: 6px
  padding: 8px 10px
  font-size: 12px
  color: #deeef5
  margin-right: 5px
  margin-bottom: 10px

</style>
