<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Portfólio Interativo</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset e Estilos Globais */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 1rem;
            position: fixed;
            width: 100%;
            z-index: 1000;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li a {
            margin: 0 15px;
            text-decoration: none;
            color: #333;
            font-weight: 500;
        }
        
        /* Seção Hero */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: #f9f9f9;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        /* Portfólio */
        .portfolio {
            padding: 6rem 2rem 4rem;
            background: #fff;
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .card {
            background: #f5f5f5;
            border-radius: 8px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        .card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .card-content {
            padding: 15px;
        }
        
        .card-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 10px;
        }
        
        .btn {
            padding: 8px 15px;
            background: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background 0.3s;
        }
        
        .btn:hover {
            background: #45a049;
        }
        
        .favorite-btn {
            background: none;
            border: none;
            font-size: 1.2rem;
            cursor: pointer;
            color: #ccc;
            transition: color 0.3s;
        }
        
        .favorite-btn.active {
            color: #ff4d4d;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#portfolio">Portfólio</a></li>
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="home" class="hero">
        <div>
            <h1>Meus Projetos</h1>
            <p>Acesse e salve seus favoritos!</p>
        </div>
    </section>
    
    <section id="portfolio" class="portfolio">
        <h2 style="text-align: center; margin-bottom: 2rem;">Portfólio</h2>
        <div class="grid">
            <!-- Item 1 -->
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Projeto 1">
                <div class="card-content">
                    <h3>Projeto 1</h3>
                    <p>Descrição breve do projeto.</p>
                    <div class="card-actions">
                        <button class="btn">Acessar</button>
                        <button class="favorite-btn"><i class="far fa-heart"></i></button>
                    </div>
                </div>
            </div>
            
            <!-- Item 2 -->
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Projeto 2">
                <div class="card-content">
                    <h3>Projeto 2</h3>
                    <p>Descrição breve do projeto.</p>
                    <div class="card-actions">
                        <button class="btn">Acessar</button>
                        <button class="favorite-btn"><i class="far fa-heart"></i></button>
                    </div>
                </div>
            </div>
            
            <!-- Item 3 -->
            <div class="card">
                <img src="https://via.placeholder.com/300x200" alt="Projeto 3">
                <div class="card-content">
                    <h3>Projeto 3</h3>
                    <p>Descrição breve do projeto.</p>
                    <div class="card-actions">
                        <button class="btn">Acessar</button>
                        <button class="favorite-btn"><i class="far fa-heart"></i></button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Função para favoritar
        document.querySelectorAll('.favorite-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                this.classList.toggle('active');
                const icon = this.querySelector('i');
                if (this.classList.contains('active')) {
                    icon.classList.replace('far', 'fas'); // Coração preenchido
                } else {
                    icon.classList.replace('fas', 'far'); // Coração vazio
                }
            });
        });
    </script>
</body>
</html>
