# Implemente em seu site, um acordeon bem bacana

#######  HTML  ####### 
## Tags HTML, você pode modificar a vontade,  menos as classes 
 <div class="acordeon-item">
        <div class="acordeon-titulo">▶ O que é GitHub?</div>
        <div class="acordeon-conteudo">
            <p>GitHub é uma plataforma de hospedagem de código para controle de versão com Git. Devs usam pra guardar projetos, colaborar e mostrar portfólio.</p>
        </div>
    </div>

    <div class="acordeon-item">
        <div class="acordeon-titulo">▶ Diferença entre Git e GitHub</div>
        <div class="acordeon-conteudo">
            <p>Git é o sistema de versionamento local. GitHub é onde você sobe esse código na nuvem.</p>
        </div>
    </div>

    <div class="acordeon-item">
        <div class="acordeon-titulo">▶ O que aprendemos  hoje? </div>
        <div class="acordeon-conteudo">
            <p>Que subir código não é bruxaria e que NPM não é GitHub. Também criou um acordeon lindo! 🚀</p>
        </div>
    </div>

#######  CSS  #######
## Aqui você pode colar no começo da pagina ou link no doctype
	<style>
        .acordeon-item {
            background: white;
            margin-bottom: 10px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .acordeon-titulo {
            background: #1e2a3a;
            color: white;
            padding: 15px;
            cursor: pointer;
            font-weight: bold;
            transition: background 0.3s;
        }

        .acordeon-titulo:hover {
            background: #0f1a24;
        }

        .acordeon-conteudo {
            max-height: 0;
            padding: 0 15px;
            background: #ffffff;
            transition: max-height 0.3s ease-out, padding 0.3s;
            overflow: hidden;
            border-left: 4px solid #1e2a3a;
        }

        .acordeon-conteudo p {
            margin: 15px 0;
        }

        /* Classe ativa (aberto) */
        .acordeon-item.ativo .acordeon-conteudo {
            max-height: 200px; /* altura suficiente pro conteúdo */
            padding: 0 15px 15px 15px;
        }
    </style>

#######  JS  ####### 
## ATENÇÃO :: aqui o js deve ficar no final do site, antes de fechar o </body>
	<script>
        // Pega todos os títulos do acordeon
        const titulos = document.querySelectorAll('.acordeon-titulo');

        titulos.forEach(titulo => {
            titulo.addEventListener('click', function() {
                // Encontra o item pai ( .acordeon-item )
                const item = this.parentElement;

                // Alterna a classe "ativo"
                item.classList.toggle('ativo');
            });
        });
    </script>
	
