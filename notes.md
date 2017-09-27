Ακολουθούν σύντομες πληροφορίες για τα requests που εκτελεί ο web client:

GET:

* {base_url}/blood-donor-registry-web-public/rest/authentication/logged-on

Επιστρέφονται τα στοιχεία του χρήστη.
Αυτά τα στοιχεία είναι παρόμοια με αυτά που επιστρέφει το  blooddonor/{id}.
Υπάρχουν μεγάλες διαφορές στη δομή τους και ορισμένα κλειδιά υπάρχουν μόνο σε
ένα από τα δύο.
Επίσης, το logged-on επιστρέφει τα ονόματα δίγλωσσα ενώ το blooddonor/{id}
επιστρέφει στη γλώσσα που ζητάει ο client.

Γλώσσες: 2

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}

Επιστρέφονται τα στοιχεία του χρήστη.
Βλέπε και authentication/logged-on.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/hbts

Στοιχεία των κέντρων αιμοδοσίας.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/oldcards
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donorcards

Επιστρέφονται τα στοιχεία των καρτών αιμοδότη.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donorcard/{id}

Επιστρέφονται τα στοιχεία μίας κάρτας αιμοδότη.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donorcard/number

Επιστρέφεται ένας αριθμός.

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donorcard/request
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/coverageDonation/history
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donation/history
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donation/alert
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donation/alert/request
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donation/next
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/request

Αν ο χρήστης έχει ζητήσει αλλαγές στα στοιχεία του, εδώ επιστρέφονται οι αρχικές τιμές
και οι τροποποιημένες. Αυτές τις τιμές τις έχει σε μορφή stringified jsons.

Γλώσσες: 2

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/region/countries

Επιστρέφονται 243 χώρες και οι κωδικοί τους σε μορφή ISO 3166-1 alpha-2, ISO
3166-1 alpha-3.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/distributionpoints/regions

Επιστρέφονται οι 13 περιφέρειες της Ελλάδος. Χρησιμοποιούνται ως
κλειδιά αναζήτησης (client side search).
Γιατί; Χρειάζεται;

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/region/regions

Επιστρέφονται οι 13 περιφέρειες της Ελλάδος. Χρησιμοποιούνται ως
κλειδιά αναζήτησης (client side search).

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/rest/blooddonor/region/cities/{regionID}

Επιστρέφονται οι πόλεις της περιφέρειας.

Γλώσσες: 1

* {base_url}/blood-donor-registry-web-public/locale/{lang}.json

Υπάρχουν 2 json:
  - en
  - el
Θα είναι καλό να σκεφτούμε αν θα χρησιμοποιηθεί.
Θετικά:
  - Ίδια λεκτικά με το web client.
Αρνητικά:
  - Μπορεί τα λεκτικά να μην ταιριάζουν στις ανάγκες της οθόνης κινητού.
    π.χ. να είναι πολύ μεγάλα.
  - Πιο δυσκίνητη/χρονοβόρα η αλλαγή/προσθήκη κάποιου λεκτικού.
  - Κατανάλωση data?

* {base_url}/rest/captcha


POST:
* {base_url}/blood-donor-registry-web-public/rest/authentication/login
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}/donation/alert

Ενεργοποίηση ή απενεργοποίηση των ειδοποιήσεων του χρήστη.

PUT:
* {base_url}/blood-donor-registry-web-public/rest/blooddonor/{id}
Αλλαγές στα στοιχεία του χρήστη όπως διεύθυνση.
Να διερευνήσουμε ποια ακριβώς στοιχεία μπορούν να τροποποιηθούν.

DELETE:
* {base_url}/blood-donor-registry-web-public/rest/authentication/logout

Σημειώσεις:
* Εκκρεμεί η καταγραφή της εγγραφής.
* Υπάρχει swagger αρχείο με αναλυτικά στοιχεία για ορισμένα requests.
