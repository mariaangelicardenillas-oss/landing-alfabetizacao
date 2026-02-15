
html_content = '''<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Método Alfabetização Express - Do Zero à Leitura em 90 Dias</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #4a4a4a;
            background-color: #faf8f5;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Badge */
        .top-badge {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a5a 100%);
            color: white;
            text-align: center;
            padding: 12px;
            font-size: 14px;
            font-weight: 600;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #faf8f5 0%, #f5efe6 100%);
            padding: 60px 0 40px;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 2.5em;
            color: #d4a574;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .hero .subtitle {
            font-size: 1.2em;
            color: #8b7355;
            margin-bottom: 30px;
            font-style: italic;
        }
        
        .hero h2 {
            font-size: 2em;
            color: #5a4a3a;
            margin-bottom: 15px;
        }
        
        .hero .description {
            font-size: 1.1em;
            color: #6b5a4a;
            max-width: 600px;
            margin: 0 auto 30px;
        }
        
        .hero-image {
            width: 100%;
            max-width: 500px;
            border-radius: 20px;
            margin: 30px auto;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        /* Offer Box */
        .offer-box {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin: 40px auto;
            max-width: 600px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            border: 2px solid #f0e6d8;
        }
        
        .offer-box h3 {
            color: #d4a574;
            font-size: 1.5em;
            margin-bottom: 20px;
        }
        
        .price {
            font-size: 2em;
            color: #5a4a3a;
            margin: 20px 0;
        }
        
        .price .old-price {
            text-decoration: line-through;
            color: #999;
            font-size: 0.6em;
            margin-right: 10px;
        }
        
        .price .new-price {
            color: #e74c3c;
            font-weight: bold;
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
            color: white;
            padding: 18px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 1.2em;
            font-weight: bold;
            margin: 20px 0;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 15px rgba(231, 76, 60, 0.3);
        }
        
        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(231, 76, 60, 0.4);
        }
        
        .urgency {
            color: #e74c3c;
            font-weight: bold;
            font-size: 0.9em;
            margin-top: 10px;
        }
        
        /* Content Sections */
        .section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2em;
            color: #5a4a3a;
            margin-bottom: 40px;
        }
        
        .section-text {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 40px;
            font-size: 1.1em;
            color: #6b5a4a;
        }
        
        /* Benefits Grid */
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .benefit-card {
            background: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            border: 1px solid #f0e6d8;
        }
        
        .benefit-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }
        
        .benefit-card h4 {
            color: #d4a574;
            margin-bottom: 10px;
            font-size: 1.2em;
        }
        
        .benefit-card p {
            color: #6b5a4a;
            font-size: 0.95em;
        }
        
        .badge {
            display: inline-block;
            background: #d4a574;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8em;
            margin-bottom: 10px;
        }
        
        /* Timeline */
        .timeline {
            background: white;
            border-radius: 20px;
            padding: 40px;
            margin: 40px 0;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
        }
        
        .timeline h3 {
            text-align: center;
            color: #5a4a3a;
            margin-bottom: 30px;
        }
        
        .timeline-item {
            display: flex;
            align-items: start;
            margin-bottom: 25px;
            padding: 20px;
            background: #faf8f5;
            border-radius: 10px;
        }
        
        .timeline-number {
            background: #d4a574;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 20px;
            flex-shrink: 0;
        }
        
        .timeline-content h4 {
            color: #5a4a3a;
            margin-bottom: 5px;
        }
        
        .timeline-content p {
            color: #6b5a4a;
            font-size: 0.95em;
        }
        
        /* Phases */
        .phases-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .phase-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            border: 1px solid #f0e6d8;
        }
        
        .phase-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            background: #f5efe6;
        }
        
        .phase-content {
            padding: 25px;
        }
        
        .phase-content h4 {
            color: #d4a574;
            margin-bottom: 5px;
        }
        
        .phase-content .weeks {
            color: #999;
            font-size: 0.9em;
            margin-bottom: 10px;
        }
        
        .phase-content p {
            color: #6b5a4a;
            font-size: 0.95em;
        }
        
        /* Bonus Section */
        .bonus-section {
            background: linear-gradient(135deg, #faf8f5 0%, #f5efe6 100%);
            padding: 60px 0;
        }
        
        .bonus-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .bonus-item {
            text-align: center;
            padding: 20px;
        }
        
        .bonus-icon {
            font-size: 3em;
            margin-bottom: 10px;
        }
        
        /* Footer CTA */
        .footer-cta {
            background: white;
            text-align: center;
            padding: 60px 20px;
            border-top: 3px solid #f0e6d8;
        }
        
        .footer-cta h2 {
            color: #5a4a3a;
            margin-bottom: 20px;
        }
        
        .guarantee {
            background: #e8f5e9;
            border-left: 4px solid #4caf50;
            padding: 20px;
            margin: 30px auto;
            max-width: 600px;
            border-radius: 0 10px 10px 0;
            text-align: left;
        }
        
        .guarantee h4 {
            color: #2e7d32;
            margin-bottom: 10px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 1.8em;
            }
            
            .hero h2 {
                font-size: 1.5em;
            }
            
            .offer-box {
                padding: 25px;
                margin: 20px;
            }
            
            .timeline-item {
                flex-direction: column;
                text-align: center;
            }
            
            .timeline-number {
                margin: 0 auto 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Top Badge -->
    <div class="top-badge">
        🚀 EDIÇÃO FUNDADOR: Você recebe 20 atividades imediatamente + o restante liberado semanalmente gratuitamente
    </div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>✨ Método Alfabetização Express</h1>
            <p class="subtitle">Transformando a hora do estudo no momento favorito da criança</p>
            
            <h2>Do Zero à Leitura em 90 Dias</h2>
            <p class="description">Método completo para crianças de 5 a 8 anos, com apenas 20 minutos por dia</p>
            
            <img src="https://images.unsplash.com/photo-1544716278-ca5e3f4abd8c?w=500&h=500&fit=crop" 
                 alt="Criança feliz lendo" class="hero-image">
            
            <!-- Offer Box -->
            <div class="offer-box">
                <h3>🎉 Oferta Especial de Lançamento</h3>
                <p>Como agradecimento por ser dos primeiros a confiar no método, você paga apenas:</p>
                <div class="price">
                    <span class="old-price">$47</span>
                    <span class="new-price">$9 hoje</span>
                </div>
                <p>e recebe acesso vitalício a todo o conteúdo (incluindo atualizações futuras).</p>
                
                <a href="#comprar" class="cta-button">Quero Ser Fundador →</a>
                
                <p class="urgency">🔥 De $47 por apenas $9 - Vagas limitadas</p>
            </div>
            
            <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?w=800&h=500&fit=crop" 
                 alt="Mãe e filho lendo juntos" style="width: 100%; max-width: 700px; border-radius: 20px; margin-top: 30px;">
        </div>
    </section>

    <!-- Emotional Section -->
    <section class="section">
        <div class="container">
            <p class="section-text" style="font-size: 1.2em; font-style: italic;">
                Imagine o <strong>brilho nos olhos</strong> do seu filho quando ele ler a primeira palavra sozinho. 
                A alfabetização não precisa ser uma batalha. Com o método certo, ela se torna uma 
                <strong>aventura diária de descobertas</strong>.
            </p>
        </div>
    </section>

    <!-- What's Included -->
    <section class="section" style="background: white;">
        <div class="container">
            <h2 class="section-title">O Que Você Vai Receber</h2>
            <p style="text-align: center; color: #6b5a4a; margin-bottom: 40px;">Acesso completo ao método para crianças de 5 a 8 anos</p>
            
            <div class="benefits-grid">
                <div class="benefit-card">
                    <span class="badge">IMEDIATO</span>
                    <div class="benefit-icon">📘</div>
                    <h4>Guia do Método</h4>
                    <p>50 páginas com o passo a passo completo para alfabetizar em 90 dias</p>
                </div>
                
                <div class="benefit-card">
                    <span class="badge">20 JÁ + 20 EM BREVE</span>
                    <div class="benefit-icon">🎮</div>
                    <h4>40 Atividades Interativas</h4>
                    <p>20 atividades disponíveis imediatamente + 20 liberadas nas próximas 4 semanas</p>
                </div>
                
                <div class="benefit-card">
                    <span class="badge">LIBERAÇÃO SEMANAL</span>
                    <div class="benefit-icon">🎬</div>
                    <h4>12 Vídeos Animados</h4>
                    <p>3 vídeos imediatos + 9 vídeos extras liberados semanalmente (sem custo adicional)</p>
                </div>
                
                <div class="benefit-card">
                    <span class="badge">BÔNUS GRADUAL</span>
                    <div class="benefit-icon">🎧</div>
                    <h4>20 Áudios Educativos</h4>
                    <p>10 áudios disponíveis agora + 10 extras liberados ao longo do programa</p>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 40px;">
                <p style="color: #6b5a4a; margin-bottom: 20px;">Conteúdo que cresce com seu filho</p>
                <p style="font-size: 1.2em; color: #999; text-decoration: line-through;">Valor normal: $47</p>
                <a href="#comprar" class="cta-button">Quero Garantir Meu Acesso Vitalício →</a>
            </div>
        </div>
    </section>

    <!-- How it Works -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">📅 Como Funciona a Liberação do Conteúdo?</h2>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-number">1</div>
                    <div class="timeline-content">
                        <h4>Hoje (Imediato)</h4>
                        <p>Guia Completo + 20 Atividades + 3 Vídeos + 10 Áudios + 3 Bônus</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-number">2</div>
                    <div class="timeline-content">
                        <h4>Semanas 2-5</h4>
                        <p>+20 atividades e +3 vídeos (total 40 atividades, 6 vídeos)</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-number">3</div>
                    <div class="timeline-content">
                        <h4>Semanas 6-8</h4>
                        <p>6 vídeos finais e +10 áudios</p>
                    </div>
                </div>
                
                <div class="timeline-item" style="background: #fff3e0;">
                    <div class="timeline-number" style="background: #ff9800;">🎁</div>
                    <div class="timeline-content">
                        <h4>Bônus Especiais</h4>
                        <p>3 bônus extras liberados após 30 dias. Você não paga nada extra!</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Learning Phases -->
    <section class="section" style="background: white;">
        <div class="container">
            <h2 class="section-title">📚 Fases de Aprendizado</h2>
            <p style="text-align: center; color: #6b5a4a; margin-bottom: 40px;">12 semanas organizadas para crianças de 5 a 8 anos</p>
            
            <div class="phases-grid">
                <div class="phase-card">
                    <img src="https://images.unsplash.com/photo-1503676260728-1c00da094a0b?w=400&h=300&fit=crop" 
                         alt="Calendário de recompensas" class="phase-image">
                    <div class="phase-content">
                        <h4>Fase 1: Consciência Fonológica</h4>
                        <p class="weeks">Semanas 1-3</p>
                        <p>10 disponíveis imediatamente + 10 na semana 2</p>
                        <span style="background: #e3f2fd; color: #1976d2; padding: 3px 10px; border-radius: 10px; font-size: 0.8em;">20 ATIVIDADES</span>
                    </div>
                </div>
                
                <div class="phase-card">
                    <img src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?w=400&h=300&fit=crop" 
                         alt="Alfabeto" class="phase-image">
                    <div class="phase-content">
                        <h4>Fase 2: Alfabeto e Letras</h4>
                        <p class="weeks">Semanas 4-6</p>
                        <p>Reconhecimento e escrita de letras</p>
                    </div>
                </div>
                
                <div class="phase-card">
                    <img src="https://images.unsplash.com/photo-1456513080510-7bf3a84b82f8?w=400&h=300&fit=crop" 
                         alt="Sílabas" class="phase-image">
                    <div class="phase-content">
                        <h4>Fase 3: Sílabas Simples</h4>
                        <p class="weeks">Semanas 7-10</p>
                        <p>10 atividades + 3 vídeos + 5 áudios</p>
                    </div>
                </div>
                
                <div class="phase-card">
                    <img src="https://images.unsplash.com/photo-1471970471555-19d4b113e9ed?w=400&h=300&fit=crop" 
                         alt="Leitura" class="phase-image">
                    <div class="phase-content">
                        <h4>Fase 4: Leitura Fluida</h4>
                        <p class="weeks">Semanas 11-12</p>
                        <p>10 atividades + 3 vídeos + 5 áudios</p>
                    </div>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 40px;">
                <a href="#comprar" class="cta-button">Sim, Quero Meu Filho Lendo em 90 Dias →</a>
                <p style="color: #e74c3c; margin-top: 15px; font-size: 0.9em;">⏰ Oferta válida por tempo limitado — Últimas vagas disponíveis</p>
            </div>
        </div>
    </section>

    <!-- Bonus Section -->
    <section class="bonus-section">
        <div class="container">
            <h2 class="section-title">🎁 Bônus Especiais</h2>
            <p style="text-align: center; color: #6b5a4a; margin-bottom: 30px;">Materiais complementares exclusivos no valor de $19</p>
            
            <div style="background: white; border-radius: 20px; padding: 40px; max-width: 800px; margin: 0 auto;">
                <h3 style="text-align: center; color: #d4a574; margin-bottom: 30px;">6 Bônus Inclusos (Valor: $19)</h3>
                
                <div class="bonus-grid">
                    <div class="bonus-item">
                        <div class="bonus-icon">🎁</div>
                        <h4>Bônus 1</h4>
                        <p style="font-size: 0.9em; color: #6b5a4a;">Material exclusivo</p>
                    </div>
                    <div class="bonus-item">
                        <div class="bonus-icon">📊</div>
                        <h4>Progress Tracking</h4>
                        <p style="font-size: 0.9em; color: #6b5a4a;">Acompanhe a evolução</p>
                    </div>
                    <div class="bonus-item">
                        <div class="bonus-icon">🎯</div>
                        <h4>Meta Semanal</h4>
                        <p style="font-size: 0.9em; color: #6b5a4a;">Organização do estudo</p>
                    </div>
                    <div class="bonus-item">
                        <div class="bonus-icon">🌟</div>
                        <h4>Recompensas</h4>
                        <p style="font-size: 0.9em; color: #6b5a4a;">Sistema de incentivo</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="footer-cta" id="comprar">
        <div class="container">
            <h2>Garanta o Futuro do Seu Filho Hoje</h2>
            <p style="font-size: 1.2em; color: #6b5a4a; margin-bottom: 30px;">
                Acesso vitalício por apenas <span style="text-decoration: line-through; color: #999;">$47</span> 
                <span style="color: #e74c3c; font-size: 1.5em; font-weight: bold;">$9</span>
            </p>
            
            <div class="guarantee">
                <h4>✅ Garantia de 7 Dias</h4>
                <p>Se você não ficar satisfeito com o método, devolvemos 100% do seu dinheiro. Sem perguntas, sem burocracia.</p>
            </div>
            
            <a href="https://hotmart.com" class="cta-button" style="font-size: 1.3em; padding: 20px 50px;">
                Quero Ser Fundador - $9 →
            </a>
            
            <p style="margin-top: 30px; color: #e74c3c; font-weight: bold;">
                🔥 Oferta por tempo limitado - Últimas vagas da Edição Fundador
            </p>
            
            <img src="https://images.unsplash.com/photo-1485546246426-74dc88dec4d9?w=600&h=400&fit=crop" 
                 alt="Criança feliz" style="width: 100%; max-width: 600px; border-radius: 20px; margin-top: 40px;">
        </div>
    </section>

    <!-- Footer -->
    <footer style="background: #5a4a3a; color: white; text-align: center; padding: 30px;">
        <p>&copy; 2025 Método Alfabetização Express. Todos os direitos reservados.</p>
        <p style="font-size: 0.9em; margin-top: 10px; opacity: 0.8;">Transformando a educação, uma criança de cada vez.</p>
    </footer>
</body>
</html>'''

# Guardar el archivo
with open('/mnt/kimi/output/index.html', 'w', encoding='utf-8') as f:
    f.write(html_content)

print("✅ Archivo HTML creado exitosamente")
print("📁 Ubicación: /mnt/kimi/output/index.html")
print(f"📊 Tamaño: {len(html_content)} caracteres")
