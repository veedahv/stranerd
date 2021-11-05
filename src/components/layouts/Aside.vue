<template>
  <div class="w-100">
        <section>
          <div class="flex space-between">
            <h2 class="section-title">Challenges</h2>
            <a href="" class="view-all flex">
              <span>view all</span>
              <img src="../../assets/right.png" class="view-icon" alt="right" />
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
  </div>
</template>

<script>
import RatingCard from "../../components/RatingCard";
import ChallengeCard from "../../components/ChallengeCard";

export default {
  name: "App",
  components: {
    RatingCard,
    ChallengeCard
  },
  data() {
    return {
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

<style scoped>
.timeline {
  background: #f7f7fc;
  padding: 5px 8px;
}
.rank-btn {
  background: #546dd3;
  color: #fff;
  padding: 10px;
}
</style>
