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
          hid: 'contact',
          name: 'description',
          content: 'Επικοινωνία με τον λογιστή Κώστα Γρηγορίου',
        },
      ],
    }
  },
}
</script>
