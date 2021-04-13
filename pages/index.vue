<template>
  <div>
    <Menu />
    <Hero :data="heroData" />
    <Cards :data="cards" :title="cardsTitle" />
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
        title: 'Λογιστικές & Φοροτεχνικές Υπηρεσίες',
        text:
          'Το γραφείο μας δραστηριοποιείται στην παροχή υψηλής ποιότητας υπηρεσιών σε λογιστικά και φοροτεχνικά θέματα που αφορούν κάθε είδους επιχειρήσεις, ελεύθερους επαγγελματίες και ιδιώτες. Με σημαντική εμπειρία σε φορολογικά, φοροτεχνικά και εργατικά θέματα, το γραφείο μας αναλαμβάνει την μηχανογραφική τήρηση όλων των κατηγορίων βιβλίων του Κ.Φ.Α.Σ  κάθε μορφής επιχείρησης και την παρακολούθηση και αντιμετώπιση όλων των φορολογικών, ασφαλιστικών και λοιπών υποχρεώσεων.',
        buttonText: 'Επικοινωνία',
        buttonHref: '/contact',
      },
      cards: {},
      cardsTitle: 'Υπηρεσίες',
      about: {
        title: 'Σχετικά με εμένα',
        text:
          'Είμαι πτυχιούχος ΑΤΕΙ Πατρών του Τμήματος Λογιστικής και κάτοχος μεταπτυχιακού διπλώματος στο Ανοιχτό Πανεπιστήμιο Κύπρου στο ΜΒΑ με κατεύθυνση Τραπεζική Χρηματοοικονομικη. Άνοιξα το δικό μου λογιστικό γραφείο τον Οκτώβριο του 2013 και κατέχω άδεια λογιστή Β΄ Τάξης. Έχω παρακολουθήσει πλήθος ενημερωτικών σεμιναρίων και ημερίδων πάνω σε θέματα εργατικών, συλλογικών συμβάσεων, φορολογικών θεμάτων, ελεγκτικής, διεθνών λογιστικών προτύπων.',
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
  async fetch() {
    this.cards = await this.$prismic.api.query(
      this.$prismic.predicates.at('document.type', 'services')
    )
  },
  head() {
    return {
      title: this.title,
      titleTemplate: '%s - Αρχική',
      meta: [
        {
          name: 'description',
          content:
            'Ο δικός σας έμπιστος λογιστής στη Λάρισα, Κώστας Γρηγορίου.',
        },
        {
          property: 'og:title',
          content: 'Κώστας Γρηγορίου',
        },
        {
          property: 'og:description',
          content:
            'Ο δικός σας έμπιστος λογιστής στη Λάρισα, Κώστας Γρηγορίου.',
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
