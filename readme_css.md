#css

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: #121212; /* Tema gelap polos */
    color: #e0e0e0;
    line-height: 1.6;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

/* Header Styles */
header {
    background: linear-gradient(135deg, #1f2a44, #3b1e5e);
    padding: 2.5rem;
    text-align: center;
    color: #fff;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.6);
}

header h1 {
    font-size: 2.8rem;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 0.5rem;
}

header p {
    font-size: 1.2rem;
    opacity: 0.85;
}

/* Main Content */
.container {
    max-width: 1400px;
    width: 90%;
    margin: 0 auto;
    padding: 2rem 0;
    flex: 1;
}

.articles {
    display: flex;
    flex-wrap: nowrap;
    gap: 2rem;
    justify-content: center; /* Memastikan kartu seimbang di tengah */
    padding: 1rem 0;
}

.article-card {
    flex: 0 0 400px; /* Lebar tetap dan seimbang */
    background: #1e1e1e;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.article-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 25px rgba(0, 0, 0, 0.7);
}

.article-content {
    padding: 1.5rem;
    text-align: left;
    height: 450px; /* Tinggi tetap untuk keseimbangan */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.article-content h2 {
    font-size: 1.6rem;
    color: #00c4cc;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
}

.article-content p {
    font-size: 1rem;
    color: #b0b0b0;
    text-align: justify;
}

/* Video Container Styles */
.video-container {
    max-width: 1400px;
    width: 90%;
    margin: 0 auto 3rem;
    padding: 0;
}

.video-title {
    font-size: 1.6rem;
    color: #00c4cc;
    text-align: center;
    margin-bottom: 1.5rem;
}

.video-wrapper {
    position: relative;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    background: #000;
    border-radius: 20px;
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
    transition: transform 0.3s ease;
}

.video-wrapper:hover {
    transform: scale(1.02);
}

.video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

/* Footer Styles */
footer {
    background: #0d0d0d;
    color: #777;
    text-align: center;
    padding: 1.5rem;
    width: 100%;
    font-size: 0.9rem;
}

/* Responsive Design */
@media (max-width: 768px) {
    header h1 {
        font-size: 2rem;
    }

    .articles {
        flex-wrap: wrap; /* Wrap pada layar kecil */
        justify-content: center;
        gap: 1.5rem;
    }

    .article-card {
        flex: 0 0 90%; /* Mengisi lebar pada layar kecil */
        max-width: 400px;
    }

    .article-content {
        height: auto; /* Tinggi menyesuaikan pada layar kecil */
    }

    .container, .video-container {
        width: 95%;
    }
}
