<script>
  import MeetupItem from "./MeetupItem.svelte";
  export let meetups = [];
</script>

<!-- id={meetup.id}
title={meetup.title}
subtitle={meetup.subtitle}
imageUrl={meetup.imageUrl}
description={meetup.description}
contactEmail={meetup.contactEmail}
address={meetup.address} -->

<section>
  {#each meetups as meetup}
    <MeetupItem {...meetup} on:del-meetup={() => alert("Delete")} />
  {/each}
</section>

<style>
  section {
    width: 100%;
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 1rem;
  }

  @media (min-width: 768px) {
    section {
      grid-template-columns: repeat(2, 1fr);
    }
  }
</style>
