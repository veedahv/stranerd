<template>
  <div class="w-100">
        <section>
          <Paginate>
            My Study
          </Paginate>
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
          </div>
          <div class="flex-m flex">
            <div class="flex-p" v-for="card in tools" :key="card">
              <ToolCard :card="card"></ToolCard>
            </div>
          </div>
        </section>
        <section>
          <Paginate>
            Test Prep
          </Paginate>
          <div class="flex flex-m">
            <div class="flex-p" v-for="prep in preps" :key="prep">
              <PrepCard :prep="prep"></PrepCard>
            </div>
          </div>
        </section>
        <section>
          <Paginate>
            FlashCards
          </Paginate>
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
          <Paginate>
            Notes
          </Paginate>
          <div class="flex flex-m">
            <div class="flex-p" v-for="(card, index) in notes" :key="index">
              <NoteCard class="h-100" :card="card"></NoteCard>
            </div>
          </div>
        </section>
        <section>
          <Paginate>
            Videos
          </Paginate>
          <div class="flex flex-m">
            <div class="flex-p" v-for="(card, index) in videos" :key="index">
              <!-- <NoteCard></NoteCard> -->
              <VideoCard class="h-100" :card="card"></VideoCard>
            </div>
          </div>
        </section>
        <section>
          <Paginate>
            Study Sets
          </Paginate>
          <div class="flex flex-m">
            <div class="flex-p" v-for="card in sets" :key="card">
              <SetCard :card="card"></SetCard>
            </div>
          </div>
        </section>
  </div>
</template>

<script>
import Paginate from "../../components/pagination/Paginate";
import ToolCard from "../../components/cards/ToolCard";
import SetCard from "../../components/cards/SetCard";
import VideoCard from "../../components/cards/VideoCard";
import NoteCard from "../../components/cards/NoteCard";
import PrepCard from "../../components/cards/PrepCard";
import FlashCard from "../../components/cards/FlashCard";
import StudyCard from "../../components/cards/StudyCard";

export default {
  name: "App",
  components: {
    Paginate,
    ToolCard,
    SetCard,
    VideoCard,
    NoteCard,
    PrepCard,
    FlashCard,
    StudyCard,
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
    };
  },
};
</script>

