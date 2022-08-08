<script>
  import Header from './UI/Header.svelte';
  import MeetupGrid from './Meetups/MeetupGrid.svelte';
  import TextInput from './UI/TextInput.svelte';
  import Button from './UI/Button.svelte';

  let title = '';
  let subtitle = '';
  let imageUrl = '';
  let description = '';
  let address = '';
  let contactEmail = '';

  let meetups = [
    {
      id: 'm1',
      title: 'This is a title',
      subtitle: 'This is a subtitle',
      imageUrl: 'https://source.unsplash.com/random/300x200',
      description:
        'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.',
      address: 'Bucarelli 1956, 6B, CABA ARG',
      contactEmail: 'sasasd@hotmail.com',
    },
    {
      id: 'm2',
      title: 'This is a title2',
      subtitle: 'This is a subtitle2',
      imageUrl: 'https://source.unsplash.com/random/300x200',
      description:
        '2Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.',
      address: 'Triunvirato 2100, CABA ARG',
    },
    {
      id: 'm3',
      title: 'This is a title3',
      subtitle: 'This is a subtitle3',
      imageUrl: 'https://source.unsplash.com/random/300x200',
      description:
        '3Lorem ipsum, dolor sit amet consectetur adipisicing elit. Enim, unde.',
    },
  ];

  function addMeetup() {
    const meetup = {
      id: 'm' + meetups.length + 1,
      title: title,
      subtitle: subtitle,
      imageUrl: imageUrl,
      description: description,
      address: address,
      contactEmail: contactEmail,
    };

    meetups = [...meetups, meetup];
    console.log(JSON.stringify(meetups));
  }
</script>

<Header />
<main>
  <form on:submit|preventDefault={addMeetup}>
    <TextInput id="title" label="Title" value={title} />
    <TextInput id="subtitle" label="Subtitle" value={subtitle} />
    <TextInput id="address" label="Address" value={address} />
    <TextInput id="imageUrl" label="Image URL" value={imageUrl} />
    <TextInput id="contactEmail" label="Email" value={contactEmail} />
    <TextInput
      controlType="textarea"
      rows="3"
      id="description"
      label="Description"
      value={description}
    />
    <Button type="submit" class="btn btn-primary" caption="Save" />
  </form>
  <MeetupGrid {meetups} />
</main>

<style>
  main {
    margin-top: 5rem;
  }

  form {
    width: 30rem;
    max-width: 90%;
    margin: auto;
  }
</style>
