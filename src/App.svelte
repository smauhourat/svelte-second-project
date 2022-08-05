<script>
  import Header from "./UI/Header.svelte";
  import MeetupItem from "./Meetups/MeetupItem.svelte";

  let meetups = [
    {
      id: Math.random(),
      title: "This is a title",
      subtitle: "This is a subtitle",
      image: "https://source.unsplash.com/random/300x200",
      content:
        "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.",
    },
    {
      id: Math.random(),
      title: "This is a title2",
      subtitle: "This is a subtitle2",
      image: "https://source.unsplash.com/random/300x200",
      content:
        "2Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.",
    },
    {
      id: Math.random(),
      title: "This is a title3",
      subtitle: "This is a subtitle3",
      image: "https://source.unsplash.com/random/300x200",
      content:
        "3Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.",
    },
  ];
</script>

<Header />

{#each meetups as meetup}
  <MeetupItem
    id={meetup.id}
    title={meetup.title}
    subtitle={meetup.subtitle}
    image={meetup.image}
    content={meetup.content}
  />
{/each}
