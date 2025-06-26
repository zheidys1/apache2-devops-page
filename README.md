# 🚀 Projeto Apache2 + HTML Personalizado no Ubuntu

Este projeto demonstra a configuração básica do servidor **Apache2** em um sistema Ubuntu, incluindo a criação de uma página HTML personalizada.

---

## 📌 Objetivo

- Instalar e ativar o servidor Apache2
- Substituir a página padrão por uma página HTML personalizada
- Compreender o funcionamento do Apache no Ubuntu

---

## ⚙️ Passos Realizados

### 1. ✅ Instalação do Apache2

```bash
sudo apt update
sudo apt install apache2 -y

2. ✅ Verificação do status do serviço
sudo systemctl status apache2

Se aparecer erro de "porta em uso", foi usado:

sudo lsof -i :80
sudo systemctl stop nginx  # ou outro serviço que estava usando a porta
sudo systemctl restart apache2

3. ✅ Criação da Página HTML

cd /var/www/html
sudo rm index.html  # Remover a página padrão
sudo nano index.html

<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>¡DevOps en Acción!</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        h1 { color: #2c3e50; }
        .logo { width: 150px; }
    </style>
</head>
<body>
    <img src="https://git-scm.com/images/logos/downloads/Git-Logo-1788C.png" alt="Git Logo" class="logo">
    <h1>¡Hola Mundo DevOps!</h1>
    <p>Servidor Apache funcionando correctamente</p>
    <p>🛠️ Próximos passos: Configurar HTTPS e um reverse proxy</p>
</body>
</html>

🌐 Teste Local

http://localhost

http://[IP_DA_VM]

✅ Resultado Final:

A página HTML personalizada foi exibida corretamente no navegador, confirmando que o Apache está em funcionamento.

📁 Estrutura de Arquivos:

 index.html

✨ Autor:

Feito por Heidys Zuniga 💙

LinkedIn | GitHub


