<template>
  <div>
    <Menu />
    <Hero :data="heroData" />
    <Cards :data="cards1" />
    <Cards :data="cards2" />
    <About :data="about" />
    <Cta :data="cta" />
    <Footer :data="footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroData: {
        title: 'Λογιστικές Υπηρεσίες',
        text:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque pulvinar purus ut pretium eleifend. Nulla eget hendrerit leo. Etiam commodo nisi nec euismod mattis. Aenean fringilla lectus quis mollis pulvinar. Nunc gravida sed quam ac tempus. Suspendisse sit amet massa at odio scelerisque mattis. Etiam efficitur nec justo sed pretium. Donec semper risus tortor, id pretium nisl facilisis in. Phasellus quis quam ipsum.',
        buttonText: 'Επικοινωνία',
        buttonHref: '/contact',
      },
      cards1: {
        title: 'Υπηρεσίες',
        card1: {
          title: 'Raclette Blueberry Nextious Level',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card2: {
          title: 'Ennui Snackwave Thundercats',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card3: {
          title: 'Selvage Poke Waistcoat Godard',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing  microdosing tousled waistcoat.',
        },
      },
      cards2: {
        title: '',
        card1: {
          title: 'Raclette Blueberry Nextious Level',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card2: {
          title: 'Ennui Snackwave Thundercats',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card3: {
          title: 'Selvage Poke Waistcoat Godard',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing  microdosing tousled waistcoat.',
        },
      },
      about: {
        title: 'Σχετικά με εμένα',
      },
      cta: {
        title: 'Επικοινωνήστε μαζί μου για μια προσφορά!',
        buttonText: 'Επικοινωνία',
        buttonLink: '/contact',
      },
      footer: {
        title: 'Κώστας Γρηγορίου',
      },
    }
  },
  head() {
    return {
      title: this.title,
      titleTemplate: '%s - Αρχική',
      meta: [
        {
          hid: 'contact',
          name: 'description',
          content:
            'Ο δικός σας έμπιστος λογιστής στη Λάρισα, Κώστας Γρηγορίου.',
        },
      ],
    }
  },
}
</script>
