<template>
  <div>
    <Menu />
    <ContactForm :data="contact" />
    <Footer :data="footer" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      contact: {
        title: 'Στείλτε μου ένα μήνυμα',
        text: 'Για οποιαδήποτε απορία ή και για να λάβετε προσφορά',
        address: 'Στρατηγού Φράγκου 26, Λάρισα 41221',
        phone: '+30 6973896755',
        email: 'kosgrigoriou@gmail.com',
        contactForm: {
          title: 'Επικοινωνία',
          text: 'Πληκτρολογήστε το μήνυμά σας παρακάτω:',
          footerText: 'Θα σας απαντήσω το συντομότερο δυνατόν.',
        },
      },
      footer: {
        title: 'Κώστας Γρηγορίου',
      },
    }
  },
  head() {
    return {
      title: this.title,
      titleTemplate: '%s - Επικοινωνία',
      meta: [
        {
          name: 'description',
          content:
            'Επικοινωνήστε με τον δικό σας έμπιστο λογιστή στη Λάρισα, Κώστα Γρηγορίου.',
        },
        {
          property: 'og:title',
          content: 'Κώστας Γρηγορίου',
        },

        {
          property: 'og:description',
          content:
            'Επικοινωνήστε με τον δικό σας έμπιστο λογιστή στη Λάρισα, Κώστα Γρηγορίου.',
        },
        {
          property: 'og:url',
          content: `${process.env.baseUrl}${this.$route.path}`,
        },
        {
          property: 'og:image',
          content: `${process.env.baseUrl}/opengraph.jpg`,
        },
      ],
    }
  },
}
</script>
