[index.html](https://github.com/user-attachments/files/22928846/index.html)
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consulenza Credito & Noleggio Auto</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Stili Generali */
        body, html {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f6f9;
            color: #333;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* HEADER (STICKY) */
        .sticky-header {
            position: sticky;
            top: 0;
            z-index: 999; 
            background-color: #1e3a5f; 
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 0 0 8px 8px; 
        }
        
        header {
            color: white;
            padding: 30px 20px;
            text-align: center;
            margin-bottom: 0; 
        }

        header h1 {
            margin: 0;
            font-size: 1.8em;
        }
        
        .content-padding {
             padding-top: 20px; 
        }

        /* SEZIONE "CHI SONO" */
        .about-me-section {
            background-color: #1e3a5f; 
            color: #f4f6f9; 
            padding: 20px;
            margin-bottom: 25px; 
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .about-me-content {
            display: flex;
            gap: 20px;
            align-items: center; 
            text-align: left;
            max-width: 100%;
            justify-content: center;
        }

        .about-me-text-group { 
            flex-grow: 0;
            max-width: 750px; 
        }
        
        /* Stile Immagine Profilo */
        .profile-photo-container {
            flex-shrink: 0; 
            text-align: center; 
            order: 2; 
        }

        .profile-photo {
            width: 160px; 
            height: 160px; 
            border-radius: 50%; 
            border: 5px solid #ffc107; 
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: block; 
            margin: 0 auto 10px auto; 
        }

        .about-me-section h3 {
            color: #ffc107; 
            margin-top: 0;
            margin-bottom: 10px;
            font-size: 1.5em;
            text-align: center; 
        }
        
        .about-me-section p {
            font-size: 1.05em;
            line-height: 1.6;
            text-align: justify; 
            margin: 15px 0 0 0;
            text-align-last: center;
        }
        
        /* NUOVO: Wrapper per affiancare Chatbot e Sidebar Contatti */
        .info-contact-wrapper {
            margin: 20px auto 0 auto;
            max-width: 1000px; /* Aumento la larghezza massima per affiancare */
            width: 100%;
            display: flex; /* Abilita l'affiancamento */
            gap: 20px;
            align-items: flex-start; /* Allinea in alto */
        }
        
        /* SEZIONE CHATBOT */
        .chatbot-section {
            flex: 2; /* Dà più spazio al chatbot (es. 66%) */
            min-width: 300px; 
            padding: 0; 
            position: relative;
            min-height: 400px;
            display: flex;
            flex-direction: column;
        }

        .chat-box {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            height: 100%;
            display: flex !important; 
            flex-direction: column;
            border: 1px solid #ddd;
        }
        
        .chat-header {
            background-color: #1e3a5f;
            color: white;
            padding: 10px;
            border-top-left-radius: 8px;
            border-top-right-radius: 8px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .chat-messages {
            flex-grow: 1;
            padding: 15px;
            overflow-y: auto;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .chat-input {
            padding: 10px;
            border-top: 1px solid #ddd;
            display: flex;
        }

        .chat-input input {
            flex-grow: 1;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 4px;
            margin-right: 10px;
        }

        .chat-input button {
            background-color: #4b7cbf;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .chat-input button:hover {
            background-color: #3a6299;
        }

        .message {
            max-width: 80%;
            padding: 8px 12px;
            border-radius: 15px;
            line-height: 1.4;
        }

        .message.bot {
            background-color: #f0f0f0;
            align-self: flex-start;
            border-bottom-left-radius: 4px;
        }

        .message.user {
            background-color: #d1e7dd; 
            align-self: flex-end;
            border-bottom-right-radius: 4px;
        }
        
        /* NUOVO: Contenitore Laterale per Pulsante Consulenza e Social */
        .contact-sidebar-right {
            flex: 1; /* Dà meno spazio alla sidebar (es. 33%) */
            min-width: 250px;
            display: flex;
            flex-direction: column;
            gap: 15px; /* Spazio tra il pulsante e i social/recensioni */
        }
        
        .flyer-button {
            transition: background-color 0.3s, transform 0.2s; 
            border: none;
            padding: 10px 20px; /* Ridotto per uniformità */
            font-size: 1.0em;    /* Ridotto per uniformità */
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            
            width: 100%; /* Larghezza piena all'interno del suo container */
            margin: 0; 
            display: block; 
            
            background-color: #009944;
            color: white;
            text-align: center;
            text-decoration: none; 
            box-sizing: border-box;
        }
        .flyer-button:hover {
            background-color: #007a33;
            transform: scale(1.02); 
        }

        /* SEZIONE SOCIAL MEDIA - Stili per il fondo pagina */
        .social-media-container-footer {
            margin-top: 0; 
            margin-bottom: 0;
            max-width: 100%; 
        }
        
        .social-media-section {
            background-color: #fff;
            padding: 15px 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            text-align: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-link {
            width: 30px; /* MODIFICATO: Uniformato alla dimensione del blocco recensioni */
            height: 30px; /* MODIFICATO: Uniformato alla dimensione del blocco recensioni */
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.15);
            transition: transform 0.2s, box-shadow 0.2s;
            text-decoration: none;
            font-size: 1.2em; /* MODIFICATO: Ridotto per uniformità */
        }

        .social-link:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .social-link svg {
            width: 40%; /* MODIFICATO: Ridotto per uniformità */
            height: 40%; /* MODIFICATO: Ridotto per uniformità */
        }
        
        .social-link.whatsapp { background-color: #25D366; color: white; }
        .social-link.facebook { background-color: #3b5998; color: white; }
        .social-link.linkedin { background-color: #0077b5; color: white; }
        .social-link.instagram { 
            /* Gradiente per Instagram */
            background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
        }
        .social-link.instagram svg { 
            fill: white; 
            stroke: white; 
            stroke-width: 0.5;
        }

        /* Griglia Prodotti */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            padding: 10px 0;
        }
        
        /* CARD PRODOTTO AGGIORNATA PER LA CENTRATURA */
        .product-card {
            all: unset;
            display: flex; /* Uso Flexbox */
            flex-direction: column; /* Organizza i contenuti verticalmente */
            justify-content: center; /* Centra verticalmente */
            align-items: center; /* Centra orizzontalmente (utile per testo breve) */
            text-align: center; /* Allinea il testo all'interno dei div */
            
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            cursor: pointer;
            transition: box-shadow 0.3s, transform 0.3s; 
            border-top: 5px solid #4b7cbf;
            width: 100%;
            min-height: 100px; /* Assicura un minimo di altezza */
            box-sizing: border-box;
        }
        
        .product-card:hover,
        .product-card:focus {
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); 
            transform: translateY(-5px); 
            outline: 2px solid #ffc107;
            outline-offset: 2px;
        }

        .product-title {
            font-size: 1.3em;
            font-weight: bold;
            color: #1e3a5f;
            margin-bottom: 5px;
        }
        
        .product-description {
            /* Assicura che la descrizione sia centrata */
            text-align: center; 
        }

        /* MODALE - ANIMAZIONE FADE-IN */
        .modal {
            display: none;
            position: fixed;
            z-index: 10000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.8);
            padding-top: 20px;
            opacity: 0; 
            transition: opacity 0.3s ease-in-out; 
        }
        
        .modal.is-visible {
            opacity: 1;
        }

        .modal-content {
            background-color: #fefefe;
            margin: 5% auto; 
            padding: 20px;
            border-radius: 8px;
            max-width: 600px;
            position: relative;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            transition: max-width 0.3s;
        }
        
        /* Stile per MODALE con FLYER Singolo */
        .modal-content.flyer-mode {
             max-width: 900px !important;
        }

        /* Stile per Galleria */
        .modal-content.gallery-mode {
             max-width: 95% !important; 
             margin: 2% auto !important; 
        }
        
        /* Galleria Verticale */
        .flyer-content-gallery {
            display: block; 
            overflow-y: auto; 
            max-height: 85vh; 
            gap: 15px; 
            padding: 15px 0;
        }
        
        .flyer-content-gallery img {
            max-width: 100%; 
            width: 100%; 
            height: auto;
            display: block; 
            margin-bottom: 25px; 
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 6px;
            min-width: 300px; 
            display: none; 
        }
        
        .close-button {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            background: none;
            border: none;
            position: absolute;
            top: 10px;
            right: 20px;
            cursor: pointer;
            z-index: 10001;
        }
        .close-button:hover,
        .close-button:focus {
            color: #333;
            text-decoration: none;
            cursor: pointer;
        }
        .visiting-card {
            text-align: center;
        }
        .visiting-card p {
            margin: 8px 0;
            font-size: 1.1em;
        }
        
        /* Stile per il blocco recensioni simulato, ora un link (A) */
        .recensioni-box-link {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 3px 5px; 
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            margin: 0 0 10px 0; 
            border-left: 4px solid #ffc107; 
            flex-wrap: wrap;
            text-align: center;
            width: 100%; 
            box-sizing: border-box;
            text-decoration: none; 
            color: inherit; 
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .recensioni-box-link:hover {
            transform: scale(1.01);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.2);
        }
        .recensioni-valutazione {
            display: flex;
            align-items: center;
            margin-right: 5px; 
        }
        .recensioni-punteggio {
            font-size: 1.3em; 
            font-weight: bold;
            color: #1e3a5f;
            margin-right: 3px; 
        }
        .recensioni-stelle {
            color: #ffc107; 
            font-size: 0.8em; 
            margin-right: 3px; 
        }
        .recensioni-testo-blocco {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            line-height: 1;
        }
        .recensioni-testo-grande {
            font-size: 1.1em; 
            font-weight: bold;
            color: #1e3a5f;
            line-height: 0.8; 
        }
        .recensioni-testo-piccolo {
            font-size: 0.6em; 
            color: #333;
            font-weight: 500;
            line-height: 1;
            margin-top: 3px; 
        }
        .recensioni-interazioni {
            width: 100%;
            text-align: center;
            margin-top: 2px; 
            font-size: 0.6em; 
            color: #4b7cbf;
            font-weight: 500;
        }
        
        /* Media Queries per la compattezza in mobile */
        @media (max-width: 768px) {
            header {
                padding: 20px 10px;
                border-radius: 0; 
            }
            .about-me-content {
                flex-direction: column-reverse; 
                align-items: center;
                text-align: center;
                justify-content: center;
            }
            .about-me-text-group { 
                max-width: 100%;
                order: 2;
            }
            .profile-photo-container {
                order: 1;
                margin-bottom: 20px;
                text-align: center;
            }
            .profile-photo {
                width: 130px; 
                height: 130px;
                margin: 0 auto;
            }
            .about-me-section h3, .about-me-section p {
                text-align: center; 
                text-align-last: center; 
            }
            .flyer-content-gallery img {
                min-width: unset; 
            }
            
            /* Su mobile, i blocchi si impilano */
            .info-contact-wrapper {
                flex-direction: column; /* Impila su mobile */
                max-width: 100%;
            }
            .chatbot-section, .contact-sidebar-right {
                min-width: 100%;
                flex: none;
            }
            /* Assicura che la sidebar (pulsante e social) vada sotto il chatbot su mobile */
            .contact-sidebar-right {
                order: 2; 
                gap: 15px; /* Spazio tra gli elementi */
            }
            .flyer-button {
                width: 100%;
                margin-top: 0;
            }
            .social-media-container-footer {
                margin-bottom: 0; /* Rimosso margine inferiore se è l'ultimo */
            }
        }
    </style>
</head>
<body>

<div class="sticky-header">
    <header>
        <h1 style="font-size: 1.8em;">Consulente Creditizio & Noleggio Auto a Lungo Termine</h1>
    </header>
</div>

<div class="container content-padding">
    
    <div class="about-me-section">
        <div class="about-me-content">
            
            <div class="profile-photo-container">
                <img id="profilePhoto" class="profile-photo" alt="Foto Profilo di Massimo Macis" src="" style="display: none;" /> 
            </div>

            <div class="about-me-text-group"> 
                <p>
                    Da oltre 20 anni, con passione e dedizione, accompagno famiglie, lavoratori e pensionati nel percorso di accesso a diverse forme di finanziamento e servizi personalizzati. La mia esperienza mi ha permesso di comprendere quanto ogni storia personale sia unica, e proprio per questo motivo credo fermamente che ogni soluzione creditizia e di noleggio auto a lungo termine debba essere studiata su misura, tenendo conto delle specifiche esigenze, dei desideri e delle possibilità di ciascuno. Il mio obiettivo è molto più che offrire una semplice consulenza: voglio costruire con te un rapporto di fiducia, basato sulla trasparenza, l’affidabilità e l’ascolto attento alle necessità. Credo che un servizio personalizzato e senza sorprese sia la chiave per aiutarti davvero a raggiungere i tuoi obiettivi, con serenità e sicurezza.
                </p>
            </div>
        </div>
    </div>

    <div class="products-grid">
        <button class="product-card" data-index="0" style="border-top-color: #1e3a5f;">
            <div class="product-title">Tutte le Offerte di Mutuo</div>
            <div class="product-description">Scopri tutte le nostre soluzioni per acquisto, ristrutturazione, giovani e green.</div>
        </button>
        
        <button class="product-card" data-index="1" style="border-top-color: #009944;">
            <div class="product-title">Cessione del Quinto</div>
            <div class="product-description">La soluzione ideale che ti permette di realizzare fino a 75.000 euro anche se sei segnalato.</div>
        </button>
        
        <button class="product-card" data-index="2" style="border-top-color: #00bfa5;">
            <div class="product-title">Prestito Personale Premium</div>
            <div class="product-description">Liquidità immediata per progetti personali.</div>
        </button>
        
        <button class="product-card" data-index="3" style="border-top-color: #00564e;">
            <div class="product-title">Anticipo TFS</div>
            <div class="product-description">Promozione Ottobre: TAN Fisso 3,80%. Anticipo del Trattamento di Fine Servizio per dipendenti pubblici.</div>
        </button>

        <button class="product-card" data-index="4" style="border-top-color: #4b7cbf;">
            <div class="product-title">Noleggio Auto a Lungo Termine</div>
            <div class="product-description">L'auto dei tuoi sogni con l'unico pensiero del carburante; il resto è tutto incluso nel canone, per privati e Partite IVA.</div>
        </button>
        
        <button class="product-card" data-index="5" style="border-top-color: #009944;">
            <div class="product-title">Conto Corrente Personalizzato</div>
            <div class="product-description">Soluzioni modulari per ogni esigenza, con canone azzerabile.</div>
        </button>

        <button class="product-card" data-index="6" style="border-top-color: #ffc107;">
            <div class="product-title">Visure Creditizie</div>
            <div class="product-description"></div> </button>
        
        <button class="product-card" data-index="7" style="border-top-color: #795548;">
            <div class="product-title">Estinzioni & Consolidamento</div>
            <div class="product-description">Unisci i tuoi debiti in un'unica rata più leggera.</div>
        </button>
        
    </div>

    <div class="info-contact-wrapper">

        <div class="chatbot-section">
            
            <div id="chat-box" class="chat-box"> 
                <div class="chat-header">
                    Assistente Creditizio & Noleggio Auto
                </div>
                <div id="chat-messages" class="chat-messages">
                    <div class="message bot">Ciao, sono l'Assistente Virtuale di Massimo Macis. In che modo posso esserti di aiuto?</div>
                </div>
                <div class="chat-input">
                    <input type="text" id="user-input" placeholder="Scrivi il tuo messaggio qui...">
                    <button onclick="sendMessage()">Invia</button>
                </div>
            </div>
        </div>
        
        <div class="contact-sidebar-right">
            
            <a href="#" id="contactButton" class="flyer-button">
                📞 RICHIEDI UNA CONSULENZA IMMEDIATA
            </a>
            
            <a href="https://www.google.com/search?q=Consulente+creditizio+%26 Noleggio+auto+a+lungo+termine&stick=H4sIAAAAAAAA_w3GQQqAIBAAwFPRM5agzmma1bV7f9hyE8EUTCF6Ti-tyzBVWTfdzTipXuoJlRJIB5u7m6PY-lFIxE0NXLO3kEvwV3bkE8EeSdtkHxughTU4MuYv5vQDLnsTIFE8racP0GO1i2EAAAA&hl=it&mat=CVm1VbSXxczQElYBYJahaahTAQ3By5HIGcFBO6pOYknYj35QLqQEDSNJH-_BcGX3L6OKi0145Azd2z726EIyGbZ_Tikl7uZIx3sPxaY0gZ_dmBjNnOpLoJ37ThZCC8vyA&authuser=0" target="_blank" class="recensioni-box-link" aria-label="Visualizza 59 recensioni su Google">
                <div class="recensioni-valutazione">
                    <span class="recensioni-punteggio">4,9</span>
                    <span class="recensioni-stelle">
                        &#9733;&#9733;&#9733;&#9733;&#9733; 
                    </span>
                </div>
                <div class="recensioni-testo-blocco">
                    <span class="recensioni-testo-grande">59</span>
                    <span class="recensioni-testo-piccolo">recensioni</span>
                </div>
                <div class="recensioni-interazioni">
                    📈 1.152 interazioni con i clienti
                </div>
            </a>
            <div class="social-media-container-footer">
                <div class="social-media-section">
                    <div class="social-links">
                        
                        <a href="https://wa.me/393473445583?text=Salve%2C%20vorrei%20informazioni%20sulle%20vostre%20offerte%20finanziarie." target="_blank" class="social-link whatsapp" aria-label="Contattami su WhatsApp">
                            <svg viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg"><path d="M12 2C6.48 2 2 6.48 2 12c0 3.2 1.54 6.09 4 7.97l-1.04 3.79 3.96-1.04c1.88 0.5 4 0.78 6.08 0.78 5.52 0 10-4.48 10-10S17.52 2 12 2zm4.7 13.91l-1.63-.8c-.3-.15-.65-.2-.99-.08l-1.42 1.42c-.2.2-.5.2-.7 0l-3.2-3.2c-.2-.2-.2-.5 0-.7l1.42-1.42c.12-.34.07-.69-.08-.99l-.8-1.63c-.15-.3-.43-.49-.78-.49H7.5c-.3 0-.5.2-.5.5s.2.5.5.5h2.15l.63.63c.2.2.5.2.7 0l3.2 3.2c.2.2.2.5 0 .7l-.63.63v2.15c0 .3.2.5.5.5s.5-.2.5-.5V14.5c0-.28.1-.55.28-.73l1.83-.88c.37-.18.78-.05 1.05.3l.8 1.63c.15.3.07.65-.21.89z"/></svg>
                        </a>
                        
                        <a href="https://www.facebook.com/massimomacis72?locale=it_IT" target="_blank" class="social-link facebook" aria-label="Visita la pagina Facebook">
                            <svg viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg"><path d="M14 13.5h2.5l1-4H14v-2c0-1.03 0-2 2-2h3V2h-3c-3.87 0-5 1.73-5 5v2.5H7v4h2v9h5v-9z"/></svg>
                        </a>
                        
                        <a href="https://www.linkedin.com/in/massimo-macis-0ab6641a4/" target="_blank" class="social-link linkedin" aria-label="Visita il profilo LinkedIn">
                            <svg viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg"><path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.381 1.11-2.5 2.48-2.5s2.48 1.119 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.965v16h4.965v-8.188c0-3.877 4.524-3.52 4.524 0v8.188h4.964v-10.932c0-7.062-8.523-7.234-9.988-3.325v-.387h-5z"/></svg>
                        </a>

                        <a href="https://www.instagram.com/massimomacis72/" target="_blank" class="social-link instagram" aria-label="Visita il profilo Instagram">
                            <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.266.069 1.646.069 4.85 0 3.204-.012 3.584-.069 4.85-0.148 3.228-1.667 4.772-4.919 4.919-1.266.058-1.646.069-4.85.069-3.204 0-3.584-.012-4.85-.069-3.252-0.148-4.771-1.691-4.919-4.919-0.058-1.266-0.069-1.646-0.069-4.85 0-3.204.012-3.584.069-4.85 0.148-3.227 1.667-4.771 4.919-4.919 1.266-0.058 1.646-0.069 4.85-0.069zM12-0.001c-3.259 0-3.667.014-4.945.074-4.435.204-6.793 2.571-7 6.953-0.06 1.278-0.076 1.686-0.076 4.945s0.016 3.667 0.076 4.945c0.207 4.382 2.571 6.749 7 6.953 1.278 0.06 1.686 0.076 4.945 0.076s3.667-0.016 4.945-0.076c4.432-0.204 6.791-2.571 6.953-6.953 0.06-1.278 0.076-1.686 0.076-4.945s-0.016-3.667-0.076-4.945c-0.162-4.383-2.527-6.749-6.953-6.953-1.278-0.06-1.686-0.076-4.945-0.076zM12 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.162 6.162 6.162 6.162-2.759 6.162-6.162c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.791-4-4s1.791-4 4-4 4 1.791 4 4c0 2.209-1.791 4-4 4zm6.406-11.845c-.796 0-1.442.646-1.442 1.442s.646 1.442 1.442 1.442 1.442-.646 1.442-1.442c0-.796-.647-1.442-1.442-1.442z"/></svg>
                        </a>

                    </div>
                </div>
            </div>
            
        </div>
        
    </div>
    </div>

<div id="flyerModal" class="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
    <button class="close-button" onclick="closeModal()" aria-label="Chiudi Modale">&times;</button>
    <div class="modal-content">
        <h2 id="modalTitle" style="position: absolute; left: -9999px;">Dettagli Prodotto/Contatto</h2>
        <div id="flyerContent" class="flyer-image-container">
            </div>
    </div>
</div>

<script>
// Nomi base dei file immagine (PLACEHOLDERS)
const IMAGE_BASE_NAMES = {
    // Struttura prodotti per i pulsanti (Indici 0-7)
    products: [
        { baseName: 'mutui_placeholder', alt: 'Galleria Tutte le Offerte di Mutuo' }, 
        { baseName: 'cessione_del_quinto', alt: 'Flyer Cessione del Quinto, soluzione fino a 75.000 euro' }, 
        { baseName: 'prestito_personale', alt: 'Flyer Prestito Personale Premium, liquidità immediata' }, 
        { baseName: 'tfs', alt: 'Flyer Anticipo TFS con TAN Fisso 3,80% per dipendenti pubblici' }, 
        { baseName: 'noleggio_auto_placeholder', alt: 'Galleria Noleggio Auto a Lungo Termine' }, 
        { baseName: 'conto_corrente_placeholder', alt: 'Galleria Conto Corrente Personalizzato' }, 
        { baseName: 'visure_creditizie_links', alt: 'Link Banche Dati Creditizie (CTC e CRIF)' }, 
        { baseName: 'estinzione_consolidamento_custom', alt: 'Dettagli Estinzioni e Consolidamento' }, // Index 7
    ],
    // Dati per la Galleria MUTUI (4 immagini)
    mutuiGallery: [
        { baseName: 'mutuo_ristrutturazione', alt: 'Flyer Mutuo Ristrutturazione che migliora l\'efficienza energetica' },
        { baseName: 'mutuo_giovani', alt: 'Flyer Mutuo Giovani Under 36' },
        { baseName: 'mutuo_abito_green', alt: 'Flyer Mutuo Abito Green per case in classe energetica A o B' },
        { baseName: 'mutuo_in_campagna', alt: 'Flyer Mutuo in Campagna per acquisto prima casa' },
    ],
    // Dati per la Galleria NOLEGGIO AUTO (4 immagini)
    noleggioGallery: [
        { baseName: 'noleggio_auto', alt: 'Offerte Noleggio Auto per Privati' },
        { baseName: 'noleggio_auto2', alt: 'Offerte Noleggio Auto per Privati e Famiglie' }, 
        { baseName: 'noleggio_auto3', alt: 'Offerte Noleggio Auto per Famiglia e Business' }, 
        { baseName: 'noleggio_auto4', alt: 'Offerte Noleggio Auto per Imprese' }, 
    ],
    // Dati per la Galleria CONTO CORRENTE (2 immagini)
    contoCorrenteGallery: [
        { baseName: 'conto_corrente', alt: 'Flyer Conto Corrente Personalizzato pagina 1' },
        { baseName: 'conto_corrente2', alt: 'Flyer Conto Corrente Personalizzato pagina 2' },
    ],
    // Altre immagini
    contactCard: 'biglietto_visita',
    profilePhoto: 'foto_lavoro_profilo_fb', 
};

/**
 * Funzioni di utilità per il caricamento immagini e la modale
 */
function createImgTagForRobustLoad(baseName, altText, isGallery = false) {
    const imgId = `flyer-img-${baseName}`;
    const style = isGallery ? 'style="display: none;"' : 'style="max-width: 100%; height: auto; display: none; margin: 0 auto;"';
    return `<img id="${imgId}" src="" alt="${altText}" ${style} />`;
}

function tryLoadImageRobust(imgElement, baseName, onLoadedCallback) {
    const possibleSrcs = [
        `images/${baseName}.jpg.jpg`, 
        `images/${baseName}.jpg`,       
        `images/${baseName}.png`,       
    ];

    function tryLoad(index) {
        if (index >= possibleSrcs.length) {
            imgElement.style.display = 'none'; 
            return;
        }

        const currentSrc = possibleSrcs[index];
        const testImage = new Image();
        
        testImage.onload = () => {
            imgElement.src = currentSrc;
            imgElement.style.display = 'block'; 
            if (onLoadedCallback) onLoadedCallback();
        };
        testImage.onerror = () => {
            tryLoad(index + 1);
        };
        
        testImage.src = currentSrc;
    }
    
    tryLoad(0);
}

function loadImagesInGallery(galleryData) {
    galleryData.forEach(data => {
        const imgElement = document.getElementById(`flyer-img-${data.baseName}`);
        if (imgElement) {
            tryLoadImageRobust(imgElement, data.baseName);
        }
    });
}

function getProfileImageSrc() {
    const imgElement = document.getElementById('profilePhoto');
    tryLoadImageRobust(imgElement, IMAGE_BASE_NAMES.profilePhoto, () => {
        imgElement.style.display = 'block'; 
    });
}

function getContactCardHTML() {
    const cardImgId = 'contactCardImage'; 
    
    const baseHTML = `
        <div class="visiting-card">
            <img id="${cardImgId}" alt="Biglietto da Visita di Massimo Macis" style="max-width: 300px; margin: 15px auto; border-radius: 5px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); display: none;" />
            
            <p>📍 Agenzia: Piazza Italia, 27, 09134 Cagliari</p>
            <p>📞 Cellulare: <a href="tel:+393473445583" style="color: #009944; text-decoration: none; font-weight: bold;">+39 3473445583</a></p>
            <p>📧 Email: <a href="mailto:massimo.macis@fb.bnpparibas.com" style="color: #009944; text-decoration: none;">massimo.macis@fb.bnpparibas.com</a></p>
            
            <a href="https://wa.me/393473445583?text=Salve%2C%20vorrei%20informazioni%20sulle%20vostre%20offerte%20finanziarie." target="_blank" style="display: inline-block; background-color: #25D366; color: white; padding: 10px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; margin-top: 15px;">
                Apri Chat WhatsApp
            </a>
        </div>
    `;

    return { html: baseHTML, imgId: cardImgId };
}

// Contenuto per il modal Visure Creditizie (Index 6)
function getVisureCreditizieHTML() {
    return `
        <div class="data-bank-section" style="padding: 20px; text-align: center;">
            <h3 style="color: #1e3a5f; margin-top: 0; font-size: 1.4em; border-bottom: 2px solid #ffc107; padding-bottom: 5px; margin-bottom: 15px;">Accesso Veloce Banche Dati Creditizie</h3>
            <p style="font-size: 1.0em; margin-bottom: 25px; color: #555;">Accedi direttamente per richiedere e scaricare la tua visura creditizia. Successivamente, ti supportero' nell'analisi dei dati.</p>
            <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
                <a href="https://consumatore.ctconline.it/sic/apri-istanza" target="_blank" rel="noopener noreferrer" style="background-color: #4b7cbf; color: white; padding: 12px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; transition: background-color 0.3s; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); flex-grow: 1; max-width: 250px;">
                    CTC - Richiesta di Accesso
                </a>
                <a href="https://www.crif.it/consumatori/soluzioni-per-te/mettinconto/" target="_blank" rel="noopener noreferrer" style="background-color: #4b7cbf; color: white; padding: 12px 20px; border-radius: 5px; text-decoration: none; font-weight: bold; transition: background-color 0.3s; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); flex-grow: 1; max-width: 250px;">
                    CRIF - Mettinconto
                </a>
            </div>
            <p style="font-size: 0.9em; margin-top: 25px; color: #777;">*Servizi forniti dalle rispettive banche dati. Per consulenza sui risultati, contatta Massimo Macis.</p>
        </div>
    `;
}

// Contenuto per il modal Estinzioni e Consolidamento (Index 7)
function getEstinzioniConsolidamentoHTML() {
    return `
        <div class="consolidation-section" style="padding: 10px; text-align: center;">
            <h3 style="color: #1e3a5f; margin-top: 0; font-size: 1.6em; border-bottom: 2px solid #ffc107; padding-bottom: 5px; margin-bottom: 20px;">Estinzioni & Consolidamento Debiti</h3>
            <p style="font-size: 1.05em; margin-bottom: 15px; color: #333; text-align: justify; line-height: 1.6;">
                Se hai più finanziamenti attivi (Prestiti Personali, Cessioni del Quinto, Carte Revolving) e desideri alleggerire il carico delle rate mensili, la soluzione di Estinzione e Consolidamento è ciò che fa per te.
            </p>
            <p style="font-size: 1.05em; margin-bottom: 30px; color: #333; text-align: justify; line-height: 1.6;">
                Questa opzione ti permette di unificare tutti i tuoi debiti in un unico nuovo finanziamento con una sola rata, spesso più bassa e con una durata maggiore. Non solo semplifichi la gestione delle scadenze, ma puoi anche ottenere liquidità aggiuntiva.
            </p>
            <a href="#" class="flyer-button" onclick="openContactCard(); return false;" 
               style="background-color: #4b7cbf; padding: 12px 20px; font-size: 1.1em; max-width: 300px; margin: 0 auto; display: block;">
                CHIEDI CONSULENZA GRATUITA
            </a>
            <p style="font-size: 0.85em; margin-top: 15px; color: #777;">Semplifica la tua situazione finanziaria con un piano su misura.</p>
        </div>
    `;
}


const modal = document.getElementById('flyerModal');
const flyerContentDiv = document.getElementById('flyerContent');
const modalContent = document.querySelector('.modal-content');
const productButtons = document.querySelectorAll('.product-card'); 
const contactButton = document.getElementById('contactButton'); // NUOVA VARIABILE

function openFlyer(index) {
    const productIndex = parseInt(index);
    flyerContentDiv.innerHTML = ''; 
    
    // CASO SPECIALE: VISURE CREDITIZIE (Index 6)
    if (productIndex === 6) {
        flyerContentDiv.innerHTML = getVisureCreditizieHTML();
        modalContent.classList.remove('flyer-mode');
        modalContent.classList.remove('gallery-mode');
        modalContent.style.maxWidth = '650px'; 
        
        modal.style.display = 'block';
        setTimeout(() => { modal.classList.add('is-visible'); }, 10); 
        document.querySelector('.close-button').focus();
        return; 
    }
    // NUOVO CASO SPECIALE: ESTINZIONI E CONSOLIDAMENTO (Index 7)
    else if (productIndex === 7) {
        flyerContentDiv.innerHTML = getEstinzioniConsolidamentoHTML();
        modalContent.classList.remove('flyer-mode');
        modalContent.classList.remove('gallery-mode');
        modalContent.style.maxWidth = '650px'; 
        
        modal.style.display = 'block';
        setTimeout(() => { modal.classList.add('is-visible'); }, 10); 
        document.querySelector('.close-button').focus();
        return;
    }
    
    let galleryData = null;

    // Gestione delle Gallerie
    if (productIndex === 0) { // Mutui
        galleryData = IMAGE_BASE_NAMES.mutuiGallery;
    } else if (productIndex === 4) { // Noleggio Auto
        galleryData = IMAGE_BASE_NAMES.noleggioGallery;
    } else if (productIndex === 5) { // Conto Corrente
        galleryData = IMAGE_BASE_NAMES.contoCorrenteGallery;
    }

    if (galleryData) {
        // Modalità Galleria
        modalContent.classList.remove('flyer-mode');
        modalContent.classList.add('gallery-mode');
        flyerContentDiv.classList.add('flyer-content-gallery');
        
        const galleryHTML = galleryData.map(data => createImgTagForRobustLoad(data.baseName, data.alt, true)).join('');
        flyerContentDiv.innerHTML = galleryHTML;
        
        loadImagesInGallery(galleryData);

    } else {
        // Modalità Flyer Singolo
        modalContent.classList.add('flyer-mode');
        modalContent.classList.remove('gallery-mode');
        flyerContentDiv.classList.remove('flyer-content-gallery');
        
        const productInfo = IMAGE_BASE_NAMES.products[productIndex];
        const imgTag = createImgTagForRobustLoad(productInfo.baseName, productInfo.alt);
        flyerContentDiv.innerHTML = imgTag;
        
        const imgElement = document.getElementById(`flyer-img-${productInfo.baseName}`);
        tryLoadImageRobust(imgElement, productInfo.baseName);
    }
    
    modal.style.display = 'block';
    setTimeout(() => { modal.classList.add('is-visible'); }, 10); 
    document.querySelector('.close-button').focus(); 
}

function openContactCard() {
    const contactData = getContactCardHTML();
    
    flyerContentDiv.innerHTML = contactData.html;
    modalContent.classList.remove('flyer-mode');
    modalContent.classList.remove('gallery-mode');
    modalContent.style.maxWidth = '500px'; 

    const cardImgElement = document.getElementById(contactData.imgId);
    tryLoadImageRobust(cardImgElement, IMAGE_BASE_NAMES.contactCard);

    modal.style.display = 'block';
    setTimeout(() => { modal.classList.add('is-visible'); }, 10); 
    document.querySelector('.close-button').focus();
}

function closeModal() {
    modal.classList.remove('is-visible');
    setTimeout(() => { 
        modal.style.display = 'none';
        modalContent.style.maxWidth = '600px'; // Reset al default
        modalContent.classList.remove('flyer-mode', 'gallery-mode');
        flyerContentDiv.classList.remove('flyer-content-gallery');
    }, 300); 
}

productButtons.forEach(button => {
    button.addEventListener('click', () => {
        openFlyer(button.getAttribute('data-index'));
    });
});

window.addEventListener('click', (event) => {
    if (event.target === modal) {
        closeModal();
    }
});

document.addEventListener('keydown', (event) => {
    if (event.key === 'Escape' && modal.classList.contains('is-visible')) {
        closeModal();
    }
});

// LISTENER AGGIUNTO: Risolve il problema del pulsante di contatto
contactButton.addEventListener('click', (event) => {
    event.preventDefault(); 
    openContactCard();
});

// Chiamata per caricare la foto profilo all'avvio
document.addEventListener('DOMContentLoaded', getProfileImageSrc);


/**
 * LOGICA CHATBOT (SEMPLIFICATA)
 */

const chatMessages = document.getElementById('chat-messages');
const userInput = document.getElementById('user-input');

// Variabile globale per mantenere lo stato della conversazione (necessaria per l'integrazione con l'API Gemini, se attiva)
let conversationHistory = [];

function appendMessage(text, sender) {
    const messageDiv = document.createElement('div');
    messageDiv.classList.add('message', sender);
    
    // Per il bot, sostituire i link e usare un parser markdown semplice
    if (sender === 'bot') {
        const processedText = text
            .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>') 
            .replace(/\[([^\]]+)\]\(([^)]+)\)/g, '<a href="$2" target="_blank">$1</a>'); 
        messageDiv.innerHTML = processedText;
    } else {
        messageDiv.textContent = text;
    }
    
    chatMessages.appendChild(messageDiv);
    // Scorri in basso
    chatMessages.scrollTop = chatMessages.scrollHeight;
}

// Funzione placeholder per simulare una risposta (Da rimuovere/sostituire se si attiva l'API)
async function getBotResponse(userMessage) {
    
    // Mostra il messaggio di caricamento
    const loadingMessage = document.createElement('div');
    loadingMessage.classList.add('message', 'bot');
    loadingMessage.id = 'temp-loading-message';
    loadingMessage.innerHTML = '... Sto elaborando la tua richiesta.';
    chatMessages.appendChild(loadingMessage);
    chatMessages.scrollTop = chatMessages.scrollHeight;

    let botResponse = '';
    const lowerCaseMessage = userMessage.toLowerCase().trim();

    // Logica di risposta semplificata
    if (lowerCaseMessage.includes('mutu') || lowerCaseMessage.includes('casa')) {
        botResponse = 'Sono disponibili diverse soluzioni per Mutui (Acquisto, Ristrutturazione, Giovani, Green). Clicca sulla card **"Tutte le Offerte di Mutuo"** per vedere i dettagli, oppure clicca sul pulsante **"RICHIEDI UNA CONSULENZA IMMEDIATA"** per un preventivo personalizzato.';
    } else if (lowerCaseMessage.includes('cessione') || lowerCaseMessage.includes('quinto')) {
        botResponse = 'La Cessione del Quinto è un finanziamento personale per dipendenti e pensionati. Trovi tutti i dettagli e i vantaggi sulla card **"Cessione del Quinto"** o possiamo fissare una [Consulenza Gratuita](https://wa.me/393473445583).';
    } else if (lowerCaseMessage.includes('noleggio') || lowerCaseMessage.includes('auto')) {
        botResponse = 'Il Noleggio Auto a Lungo Termine è un\'ottima soluzione per privati e Partite IVA. Clicca sulla card **"Noleggio Auto a Lungo Termine"** per la nostra gallery di offerte o invia una richiesta tramite [WhatsApp](https://wa.me/393473445583).';
    } else if (lowerCaseMessage.includes('contatt') || lowerCaseMessage.includes('parlare') || lowerCaseMessage.includes('chiama')) {
        botResponse = 'Certamente! Il modo più rapido è cliccare sul pulsante verde **"RICHIEDI UNA CONSULENZA IMMEDIATA"** in alto a destra, oppure puoi contattare Massimo Macis via [WhatsApp](https://wa.me/393473445583) o [Telefono: 3473445583](tel:+393473445583).';
    } else if (lowerCaseMessage.includes('tfs')) {
        botResponse = 'L\'Anticipo TFS ti permette di ottenere fino al 100% della liquidazione in attesa della pensione, con un TAN Fisso del 3,80% (Promozione Ottobre). Trovi il link e i dettagli nella card **"Anticipo TFS"**.';
    } else if (lowerCaseMessage.includes('ciao') || lowerCaseMessage.includes('salve')) {
        botResponse = 'Ciao! Come posso esserti utile oggi? Puoi chiedermi informazioni sui Mutui, la Cessione del Quinto o il Noleggio Auto.';
    } else if (lowerCaseMessage.includes('visura') || lowerCaseMessage.includes('crif') || lowerCaseMessage.includes('ctc')) {
        botResponse = 'Per accedere alle banche dati creditizie (CRIF e CTC), clicca sulla card **"Visure Creditizie"**. Una volta scaricata la tua visura, sarò lieto di analizzarla con te.';
    } else if (lowerCaseMessage.includes('consolidamento') || lowerCaseMessage.includes('estinzione')) {
        botResponse = 'Per unire tutti i tuoi debiti in un\'unica rata, consulta la card **"Estinzioni & Consolidamento"**. Ti aiuteremo a semplificare la gestione finanziaria e a ottenere liquidità aggiuntiva.';
    } else {
        botResponse = 'Sono un assistente virtuale e rispondo a domande sui nostri servizi. Per informazioni su Mutui, Cessione del Quinto, Noleggio Auto o altri servizi, chiedi pure! Se preferisci, puoi sempre cliccare su **"RICHIEDI UNA CONSULENZA IMMEDIATA"**.';
    }
    
    // Rimuovi il messaggio di attesa
    const loadingMessageToRemove = document.getElementById('temp-loading-message');
    if (loadingMessageToRemove) {
        loadingMessageToRemove.remove();
    }

    // Simulazione di ritardo per l'esperienza utente
    setTimeout(() => {
        appendMessage(botResponse, 'bot');
    }, 500); 
    
    // Nota: L'integrazione con l'API Gemini è disattivata in questo esempio per semplicità e costi. 
    // Per attivarla, sarebbe necessario decommentare la parte di codice relativa all'API.
}

function sendMessage() {
    const message = userInput.value.trim();
    if (message === '') return;

    appendMessage(message, 'user');
    userInput.value = '';
    
    // AGGIORNA STORIA: Aggiungi il messaggio dell'utente alla cronologia
    conversationHistory.push({ role: 'user', parts: [{ text: message }] });

    // Chiama la risposta del bot
    getBotResponse(message);
}

userInput.addEventListener('keydown', (event) => {
    if (event.key === 'Enter') {
        sendMessage();
    }
});

// Inizializza la storia della conversazione con il messaggio di benvenuto del bot
conversationHistory.push({ 
    role: 'model', 
    parts: [{ 
        text: "Ciao, sono l'Assistente Virtuale di Massimo Macis. In che modo posso esserti di aiuto?" 
    }] 
});
</script>

</body>
</html>
