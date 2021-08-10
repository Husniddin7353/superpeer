<template>
  <div id="app">
      <Header/>
      <Host/>
      <Magic :magic="magic" :img="magic.img" :profile="magic.profile" :name="magic.name" :title="magic.title" :text="magic.text" :date="magic.date" :btn="magic.btn"/>
      <Featured/>
      <Foryou :foryou="foryou" :img="foryou.img" :title="foryou.title" :text="foryou.title" />
      <Slider :slider="slider" :text="slider.text" />
      <Introducing :introducing="introducing" :img="introducing.img" :title="introducing.title" :text="introducing.text" />
      <Become/>
      <Footer/>
  </div>
 
</template>

<script>
import Header from '@/components/Header.vue'
import Host from '@/components/Host.vue'
import Magic from '@/components/Magic.vue'
import Featured from '@/components/Featured.vue'
import Foryou from '@/components/Foryou.vue'
import Slider from '@/components/Slider.vue'
import Introducing from '@/components/Introducing.vue'
import Become from '@/components/Become.vue'
import Footer from '@/components/Footer.vue'
export default {
  components:{
    Header,
    Host,
    Magic,
    Featured,
    Foryou,
    Slider,
    Introducing,
    Become,
    Footer
  },

  data(){
    return{
      magic:[
        { img: require('@/assets/magic1.png') ,
          profile : require ('@/assets/profile1.png'),
          name:'Dawn Dickson',
          title:"Masterclass on Fundraising Strategies",
          date:'September 9, 2021',
          text: 'Entry-level strategies from an expert in entrepreneurship, business development and fundraising. The first female founder to raise $1M> in an equity crowdfunding campaign will teach you the best in investment, crowdfunding and overall fundraising strategies to capitalize your business at every level.',
          btn : false
          },

          { img: require('@/assets/magic2.png') ,
          profile : require ('@/assets/profile2.png'),
          name:'Thomas Hopkins',
          btn : false,
          title:"Paid Marketing",
          date:'September 9, 2021',
          text: 'Over the past 7 years I\'ve unlocked company growth potential for brands like Lyft and Masterclass – after this series, you will too. Discover what makes a successful paid marketing campaign and how to scale a revenue-generating system.'},

          { img: require('@/assets/magic3.png') ,
          profile : require ('@/assets/profile3.png'),
          name:'Alice Johnson',
          btn : false,
          title:"Find Your True Love, your TwinFlame®",
          date:'July 26, 2021',
          text: 'I\'m an 8th-generation psychic, and together we\'ll discover how your aura operates and the magic you have within to facilitate self-love and romantic love. If you’re looking for your Twinflame®, your true love, or you’re ready to find yourself, this is the course for you. '},

          { img: require('@/assets/magic4.png') ,
          profile : require ('@/assets/profile4.png'),
          name:'Mark Wahlbeck',
          btn : false,
          title:"Fiction Writing For Absolute Beginners: How To Publish Your First Story",
          date:'August 2, 2021',
          text: 'Writing can be hard! Publishing can be even harder! In this Series not only will you learn how to write good fiction, you’ll also learn how to publish your writing.'},

          { img: require('@/assets/magic5.png') ,
          profile : require ('@/assets/profile5.png'),
          name:'Jason Akel',
          btn : false,
          title:"Self-Hypnosis and HypnoTherapy Adventures",
          date:'July 24, 2021',
          text: 'Stop being so critical of yourself and overanalyzing everything. Discover the power of hypnosis and hypnotherapy: you could be living a more confident, free-thinking life. For first-timers and experienced meditators – relax, learn and get motivated.'},

          { img: require('@/assets/magic6.png') ,
          profile : require ('@/assets/profile6.png'),
          name:'Tristan Pollock',
          btn : false,
          title:"Movement Building",
          date:'July 28, 2021',
          text: 'Calling all startup founders, entrepreneurs, execs, and business leaders. Learn to build communities, make a pitch deck and create a movement around a company mission. Global impact-driven movements have all started somewhere, and today it\'s here'},

          { img: require('@/assets/magic7.png') ,
          profile : require ('@/assets/profile7.png'),
          name:'Jose Caya',
          btn : false,
          title:"Pitch Deck Examples & How to Class",
          date:'August 6, 2021',
          text: 'We’ve looked at thousands of investor pitch decks, so we know what a good one looks like. Learn how to tell your company story in a way that excites investors. See what the pros in the game did – AirBnb and Uber – and get set up to pitch a homerun. '},

          { img: require('@/assets/magic8.png') ,
          profile : require ('@/assets/profile8.png'),
          name:'Devrim Yasar',
          btn : false,
          title:"Starting your Business",
          date:'August 29, 2021',
          text: 'Got an idea for a start-up, want to raise money or start a business? These interactive lessons will let you take the stage and pitch your idea. Join me on Superpeer to learn about mentorship, investors, cofounders, fundraising and telling your story. '},

          { img: require('@/assets/magic9.png') ,
          profile : require ('@/assets/profile9.png'),
          name:'Armagan Amcalar',
          btn : false,
          title:"Public Speaking",
          date:'August 23, 2021',
          text: 'You should be giving a talk this year: Discover the super-hero speaker in you from someone who has been doing it for 20 years. An interactive workshop where you\'ll create your own conference speech and master how to speak confidently to an audience. '},

          { img: require('@/assets/magic10.png') ,
          profile : require ('@/assets/profile10.png'),
          name:'Jasmine Lawrence',
          title:"You can’t Entrepreneur without PM",
          date:'August 25, 2021',
          btn : false,
          text: 'Get insight into the life and career lessons learned from being a CEO and product manager. Learn about entrepreneurship: doing the big pitch, falling in love with the problem, and when to side hustle. Strategize and execute your big idea. '},

      ],

      foryou:[
        {
          img:require('@/assets/for.png'),
          title: 'Engage with your audience',
          text:'Connect with your subscribers through interactive livestreams, 1:1s, and our newest feature, Series.'
        },

        {
          img:require('@/assets/for2.png'),
          title: 'Manage easier',
          text:'We take care of scheduling, payments, and protecting your privacy, so that you don’t have to.'
        },

        {
          img:require('@/assets/for3.png'),
          title: 'Earn, your way',
          text:'Set your own rates and earn revenue through weekly livestreams, channel subscriptions, and even donations.'
        },
      ],

      slider:[
        {
          text:'“I\'ve been using Superpeer with about 10-12 calls per week, and so far the experience has been flawless.”'
        },
        {
          text:'“I\'ve been about  and so far the experience has been flawless.”'
        },

        {
          text:'“Superpeer with about 10-12 calls per week, and so far the experience has been flawless.”'
        },

        {
          text:'“I\'ve been  with about 10-12 calls per week, and so far the experience has been flawless.”'
        }
      ],

      introducing:[
        {
          img:require('@/assets/introducing1.png'),
          title:'Customize the content',
          text:'Organize your live streams, pre-recorded videos, and hosted events into purchasable content packages for your audience.'
        },

        {
          img:require('@/assets/introducing2.png'),
          title:'Set the pace',
          text:'Organize your live streams, pre-recorded videos, and hosted events into purchasable content packages for your audience.'
        },

        {
          img:require('@/assets/introducing3.png'),
          title:'Immerse the audience',
          text:'Organize your live streams, pre-recorded videos, and hosted events into purchasable content packages for your audience.'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
body{
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container{
  max-width: 1190px;
  margin: 0 auto;
}

a{
  text-decoration: none !important;
  color: black ;
}
.btn{
  outline: none !important;
  box-shadow: none !important;
}


.become-btn{
  font-size: 16px;
  line-height: 22px;
  text-transform: uppercase;
  color: #222222;
  background: #FFD338;
  border-radius: 8px;
  padding: 12px 16px;

  svg{
    margin-right: 8px;
  }

  &:hover{
    background-color: #fdc703;
    color: white;
    transition: all 0.2s;
  }
}
</style>
