<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="app w-100">
    <div class="body w-100 grid">
      <nav class="side-nav">
        <SideNav class="h-100"></SideNav>
      </nav>
      <div class="left-header">
        <div class="flex header-flex">
          <div class="input-box btn w-100 flex">
            <input
              type="text"
              placeholder="Search for anything"
              class="input w-100 btn"
            />
            <button class="search btn">
              <img
                src="./assets/search.png"
                class="search-icon header-icon"
                alt="coin"
              />
            </button>
          </div>
          <button class="header-btn btn">
            <img src="./assets/add.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="./assets/bell.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="./assets/grad.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="./assets/chatbubble.png" class="header-icon" alt="coin" />
          </button>
          <button class="header-btn btn">
            <img src="./assets/person.png" class="header-icon" alt="coin" />
          </button>
        </div>
      </div>
      <div class="right-header">
        <div class="card header-card">
          <div class="card-body card-header">
            <div class="card-flex flex space-between">
              <span>
                <div class="flex">
                  <span>10k</span>
                  <img src="./assets/coin.png" class="coin-icon" alt="coin" />
                </div>
              </span>
              <span>
                <div class="flex">
                  <img src="./assets/add.png" class="header-icon" alt="coin" />
                </div>
              </span>
              <span>
                <div class="flex">
                  <span>250</span>
                  <img src="./assets/coin-l.png" class="coin-icon" alt="coin" />
                </div>
              </span>
            </div>
          </div>
        </div>
      </div>
      <main class="main">
        <section>
          <div class="flex space-between">
            <h2 class="section-title">My Study</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p">
              <StudyCard courseType="video"></StudyCard>
            </div>
            <div class="flex-p">
              <StudyCard courseType="note"></StudyCard>
            </div>
            <div class="flex-p">
              <FlashCard></FlashCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between">
            <h2 class="section-title">Study Tools</h2>
            <!-- <a href="" class="view-all flex">
              <span>view all</span>
              
              <img src="./assets/right.png" class="view-icon" alt="right" />
              </a> -->
          </div>
          <div class="flex-m flex">
            <div class="flex-p" v-for="card in tools" :key="card">
              <ToolCard :card="card"></ToolCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between section-heading">
            <h2 class="section-title">Test Prep</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p" v-for="prep in preps" :key="prep">
              <PrepCard :prep="prep"></PrepCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between section-heading">
            <h2 class="section-title">Flashcards</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p">
              <FlashCard></FlashCard>
            </div>
            <div class="flex-p">
              <FlashCard></FlashCard>
            </div>
            <div class="flex-p">
              <FlashCard></FlashCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between section-heading">
            <h2 class="section-title">Notes</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p" v-for="(card, index) in notes" :key="index">
              <NoteCard class="h-100" :card="card"></NoteCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between section-heading">
            <h2 class="section-title">Videos</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p" v-for="(card, index) in videos" :key="index">
              <!-- <NoteCard></NoteCard> -->
              <VideoCard class="h-100" :card="card"></VideoCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between">
            <h2 class="section-title">Study Sets</h2>
            <div class="paginate flex">
              <span class="arrow">
                <img src="./assets/arrow-l.png" class="arrow-img" alt="" />
              </span>
              <span class="circle c-active"></span>
              <span class="circle"></span>
              <span class="circle"></span>
              <span class="arrow">
                <img src="./assets/arrow-r.png" class="arrow-img" alt="" />
              </span>
            </div>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="flex flex-m">
            <div class="flex-p" v-for="card in sets" :key="card">
              <SetCard :card="card"></SetCard>
            </div>
            <!-- <div class="flex-p">
              <SetCard courseType="video"></SetCard>
            </div>
            <div class="flex-p">
              <SetCard courseType="video"></SetCard>
            </div> -->
          </div>
        </section>
      </main>
      <aside class="aside">
        <section>
          <div class="flex space-between">
            <h2 class="section-title">Challenges</h2>
            <a href="" class="view-all flex">
              <span>view all</span>

              <img src="./assets/right.png" class="view-icon" alt="right" />
            </a>
          </div>
          <div class="">
            <div class="" v-for="card in challenges" :key="card">
              <ChallengeCard :card="card"></ChallengeCard>
            </div>
          </div>
        </section>
        <section>
          <div class="flex space-between">
            <h2 class="section-title">Ranking</h2>
            <div class="">
              <select name="" id="" class="timeline btn">
                <option value="Daily">Daily</option>
              </select>
            </div>
          </div>
          <div class="">
            <div class="" v-for="card in rankings" :key="card">
              <RatingCard :card="card"></RatingCard>
            </div>
            <button class="btn rank-btn w-100">Leaderboard</button>
          </div>
        </section>
      </aside>
    </div>
  </div>
</template>

<script>
import ToolCard from "./components/ToolCard";
import RatingCard from "./components/RatingCard";
import ChallengeCard from "./components/ChallengeCard";
import SetCard from "./components/SetCard";
import VideoCard from "./components/VideoCard";
import NoteCard from "./components/NoteCard";
import PrepCard from "./components/PrepCard";
import FlashCard from "./components/FlashCard";
import StudyCard from "./components/StudyCard";
import SideNav from "./components/SideNav";
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  components: {
    ToolCard,
    RatingCard,
    ChallengeCard,
    SetCard,
    VideoCard,
    NoteCard,
    PrepCard,
    FlashCard,
    StudyCard,
    SideNav,
    // HelloWorld
  },
  data() {
    return {
      tools: [
        {
          type: "card",
          title: "Study with Flashcards",
          note:
            "Scientifically proven to improve memory and make studying easier.",
          btn: "Create a Flashcard",
        },
        {
          type: "file",
          title: "Organize your Study",
          note:
            "Put flashcards, notes and videos with the same aim together in a folder.",
          btn: "Create a Study Set",
        },
        {
          type: "location",
          title: "Find more resources",
          note:
            "Browse through a library of flashcards, notes, videos and sets to study with.",
          btn: "Explore",
        },
      ],
      preps: [
        {
          title: "JAMB",
          note: "Gateway exams for tertiary level instituitions in Nigeria.",
          paid: true,
        },
        {
          title: "SAT",
          note:
            "The SAT is a standardized test widely used for college admissions in the USA",
          paid: false,
        },
        {
          title: "WAEC",
          note:
            "Standardized test for West African secondary education completion.",
          paid: true,
        },
      ],
      notes: [
        {
          desc: "Work and Energy - Introduction to University physics",
          paid: true,
        },
        {
          desc: "Integration and Multivariate Calculus for Year 1",
          paid: false,
        },
        {
          desc: "Work and Energy - Introduction to University physics",
          paid: true,
        },
      ],
      videos: [
        {
          desc: "Work and Energy - Introduction to University physics Videos",
          paid: true,
        },
        {
          desc: "Integration and Multivariate Calculus for Year 1 - Videos",
          paid: false,
        },
        {
          desc: "Work and Energy - Introduction to University physics - Videos",
          paid: true,
        },
      ],
      sets: [
        {
          desc: "Complete resources for 100l CEG - UNILAG",
          paid: true,
          tags: ["card", "note", "video"],
        },
        {
          desc: "WAEC Physics - All you need for A1",
          paid: false,
          tags: ["card", "note", "video"],
        },
        {
          desc: "Organized MEG notes - 100l to 500l - UNILAG",
          paid: true,
          tags: ["note"],
        },
      ],
      challenges: [
        {
          desc: "Reach the rank of ",
          em: "Comrade",
          progress: "68%",
        },
        {
          desc: "Answer 30 questions",
          em: "",
          progress: "58%",
        },
        {
          desc: "Get 30 best answers",
          em: "",
          progress: "48%",
        },
        {
          desc: "5 days login streak",
          em: "",
          progress: "38%",
        },
      ],
      rankings: [
        {
          sn: 122,
          title: "Jerry Maguire",
          rank: 14,
        },
        {
          sn: 123,
          title: "Jerry Maguire",
          rank: 14,
        },
        {
          sn: 124,
          title: "Timmy Neutron",
          rank: 14,
        },
        {
          sn: 125,
          title: "Jerry Maguire",
          rank: 14,
        },
        {
          sn: 126,
          title: "Jerry Maguire",
          rank: 14,
        },
      ],
    };
  },
};
</script>

<style>
* {
  font-family: "Raleway", sans-serif;
  color: #4d5c6f;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  max-width: 1700px;
  margin: 0 auto;
}
a {
  text-decoration: none;
  display: inline-block;
}
ul {
  list-style: none;
}
section {
  margin-top: 30px;
  margin-bottom: 30px;
}
.section-title {
  margin-bottom: 15px;
  margin-top: 15px;
  font-size: 16px;
}
.btn {
  background: transparent;
  outline: none;
  border: none;
  border-radius: 7px;
}
.bg-dark-gray {
  color: #fff;
  border: 1px solid #4d5c6f;
  background: #4d5c6f;
}
.header-flex.flex {
  gap: 20px;
}
.input-box,
.header-btn {
  background: #f7f7fc;
  padding: 8px 15px;
}
input {
  font-size: 15px;
}
.paginate {
  gap: 4px;
  align-items: center;
}
.arrow-img {
  width: 8px;
}
.circle {
  height: 5px;
  width: 5px;
  border: 1px solid #c7d6e3;
  background: #c7d6e3;
  border-radius: 5px;
}
.c-active {
  border: 1px solid #546DD3;
  background: #546DD3;
}
.timeline {
  background: #f7f7fc;
  padding: 5px 8px;
}
.header-btn:hover {
  background: #546dd3;
  cursor: pointer;
}
.header-icon {
  width: 16px;
}
.header-card {
  padding: 8px 25px;
  border-radius: 8px;
}
.header-card .flex {
  gap: 4px;
}
.coin-btn {
  padding: 2px 3px;
}
.h-100 {
  height: 100%;
}
.w-100 {
  width: 100%;
}
.my {
  margin-top: 8px;
  margin-bottom: 8px;
}
.view-all span {
  color: #546dd3;
  font-weight: 500;
  font-size: 14px;
}
.instructor {
  font-size: 14px;
}
.view-all.flex {
  align-items: center;
  gap: 4px;
}
.person-icon,
.card-icon {
  width: 20px;
}
.coin-icon {
  width: 18px;
}
button.btn:hover {
  cursor: pointer;
}
.coin-btn span {
  color: #fff;
}
.star {
  width: 16px;
}
.flex {
  display: flex;
  align-items: center;
}
.grid {
  display: grid;
  gap: 20px;
  grid-template-columns: 3fr 12fr 4fr;
  grid-template-areas:
    "sideNav leftHeader rightHeader"
    "sideNav main aside";
}
.side-nav {
  grid-area: sideNav;
}
.left-header {
  grid-area: leftHeader;
  padding-top: 40px;
}
.right-header {
  padding-right: 20px;
  grid-area: rightHeader;
  padding-top: 40px;
}
.main {
  grid-area: main;
  padding-bottom: 25px;
}
p {
  font-size: 15px;
}
.aside {
  grid-area: aside;
  padding-right: 20px;
}
.space-between {
  justify-content: space-between;
}
/* .items-start {
  align-items: flex-start;
} */
.flex-m {
  margin: 0 -10px;
  align-items: stretch;
}
.flex-p {
  padding: 0 10px;
  flex: 1;
}
.card {
  /* background: #f7f7fc; */
  border-radius: 10px;
  background: #f7f7fc;
}
.preview-box {
  background: #c7d6e3;
  border-radius: 10px;
}
.preview-box .btn {
  color: #fff;
  text-transform: uppercase;
  font-weight: 600;
}
.rank-btn {
  background: #546dd3;
  color: #fff;
  padding: 10px;
}
</style>
