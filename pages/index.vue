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
        title: 'Λογιστικές & Φοροτεχνικές Υπηρεσίες',
        text:
          'Το γραφείο μας δραστηριοποιείται στην παροχή υψηλής ποιότητας υπηρεσιών σε λογιστικά και φοροτεχνικά θέματα που αφορούν κάθε είδους επιχειρήσεις, ελεύθερους επαγγελματίες και ιδιώτες. Με σημαντική εμπειρία σε φορολογικά, φοροτεχνικά και εργατικά θέματα, το γραφείο μας αναλαμβάνει την μηχανογραφική τήρηση όλων των κατηγορίων βιβλίων του Κ.Φ.Α.Σ  κάθε μορφής επιχείρησης και την παρακολούθηση και αντιμετώπιση όλων των φορολογικών, ασφαλιστικών και λοιπών υποχρεώσεων.',
        buttonText: 'Επικοινωνία',
        buttonHref: '/contact',
      },
      cards1: {
        title: 'Υπηρεσίες',
        card1: {
          title: 'Φορολογικές δηλώσεις',
          text:
            'Αναλαμβάνω να πραγματοποιήσω τις φορολογικές δηλώσεις σας, είτε πρόκειται για δηλώσεις φυσικών Προσώπων ή επιχειρήσεων.',
        },
        card2: {
          title: 'Συστάσεις - Ενάρξεις - Διακοπές - Μεταβολές',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card3: {
          title: "Τήρηση βιβλίων Β' και Γ' κατηγορίας",
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing  microdosing tousled waistcoat.',
        },
      },
      cards2: {
        title: '',
        card1: {
          title: 'Ενημέρωση βιβλίου απογραφής',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card2: {
          title: 'Περιοδικές και εκκαθαριστικές δηλώσεις ΦΠΑ',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing microdosing tousled waistcoat.',
        },
        card3: {
          title: 'Προσωρινές και οριστικές δηλώσεις ΦΜΥ',
          text:
            'Photo booth fam kinfolk cold-pressed sriracha leggings jianbing  microdosing tousled waistcoat.',
        },
      },
      about: {
        title: 'Σχετικά με εμένα',
        text:
          'Είμαι πτυχιούχος ΑΤΕΙ Πατρών του Τμήματος Λογιστικής και κάτοχος μεταπτυχιακού διπλώματος στο Ανοιχτό Πανεπιστήμιο Κύπρου και κάτοχος ΜΒΑ με κατεύθυνση Τραπεζική Χρηματοοικονομικη. Άνοιξα το δικό μου λογιστικό γραφείο τον Οκτώβριο του 2013 και κατέχω άδεια λογιστή Β΄ Τάξης. Έχω παρακολουθήσει πλήθος ενημερωτικών σεμιναρίων και ημερίδων πάνω σε θέματα εργατικών, συλλογικών συμβάσεων, φορολογικών θεμάτων, ελεγκτικής, διεθνών λογιστικών προτύπων.',
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
