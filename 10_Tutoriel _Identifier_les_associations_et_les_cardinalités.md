### The associations between `CLIENT`, `COMMANDE`and `PRODUIT`:
CLIENT---> [make] --->  COMMANDE 
COMMANDE ---> [present] ---> PRODUIT
PRODUIT ---> [tooked by] ---> OMMANDE
### Determining the cardinalities 
CLIENT_____(0,N) ______make_____(1,N)_____COMMANDE
COMMANDE_____(1,N)______have_______(0,N)______PRODUIT
## the ilustrator image
```mermaid
erDiagram
    CLIENT ||--o{ COMMANDE : places
    COMMANDE |{--o{ PRODUCT : contains {
        string quantite_commande
    }
    
    CLIENT {
        string id PK
        string name
        string email
    }
    COMMANDE {
        string id PK
        string commande_number
        string date_commande
    }
    PRODUCT {
        string id PK
        string product_name
        string product_price
    }