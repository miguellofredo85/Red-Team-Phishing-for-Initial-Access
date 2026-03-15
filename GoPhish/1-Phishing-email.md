## Criar Template
<img width="1850" height="966" alt="Image" src="https://github.com/user-attachments/assets/676322f6-fb9e-4606-8b13-3e0182de8659" />


## HTML template

```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>Acme Security - Autenticação Multifator</title>
    <style>
        /* Reset e estilos gerais para clientes de email */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', 'Inter', -apple-system, BlinkMacSystemFont, 'Helvetica Neue', Arial, sans-serif;
            background-color: #f4f6f9;
            color: #1e293b;
            line-height: 1.6;
        }
        
        .email-wrapper {
            width: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 40px 20px;
        }
        
        .email-container {
            max-width: 600px;
            margin: 0 auto;
            background: #ffffff;
            border-radius: 24px;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        /* Header com gradiente */
        .email-header {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            padding: 32px 40px;
            text-align: center;
        }
        
        .header-logo {
            width: 64px;
            height: 64px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 16px;
            color: white;
            font-size: 28px;
            font-weight: bold;
            backdrop-filter: blur(10px);
        }
        
        .email-header h1 {
            color: white;
            font-size: 24px;
            font-weight: 600;
            margin: 0;
            text-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        .email-header p {
            color: rgba(255,255,255,0.9);
            font-size: 16px;
            margin: 8px 0 0;
        }
        
        /* Conteúdo principal */
        .email-content {
            padding: 40px;
        }
        
        .greeting {
            font-size: 18px;
            font-weight: 500;
            margin-bottom: 24px;
            color: #1e293b;
        }
        
        .greeting strong {
            color: #6366f1;
        }
        
        .message-box {
            background: #f8fafc;
            border-left: 4px solid #6366f1;
            padding: 24px;
            border-radius: 12px;
            margin-bottom: 32px;
        }
        
        .message-box h3 {
            margin: 0 0 12px 0;
            color: #1e293b;
            font-size: 18px;
            font-weight: 600;
        }
        
        .message-box ul {
            margin: 0;
            padding-left: 20px;
            color: #475569;
        }
        
        .message-box li {
            margin-bottom: 8px;
        }
        
        .highlight-box {
            background: #eff6ff;
            border: 1px solid #c7d2fe;
            border-radius: 12px;
            padding: 24px;
            margin: 32px 0;
            text-align: center;
        }
        
        .highlight-box p {
            margin: 0 0 16px;
            color: #1e293b;
            font-weight: 500;
        }
        
        /* Botão principal (o link do lure) */
        .btn-primary {
            display: inline-block;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            color: #ffffff !important;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            padding: 16px 40px;
            border-radius: 12px;
            box-shadow: 0 10px 25px -5px rgba(99, 102, 241, 0.4);
            transition: all 0.3s ease;
            border: none;
            margin: 16px 0;
        }
        
        /* Fallback para clientes que não suportam gradientes */
        .btn-primary-fallback {
            background-color: #6366f1;
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 18px;
            padding: 16px 40px;
            border-radius: 12px;
            display: inline-block;
            margin: 16px 0;
        }
        
        .security-notice {
            background: #fef9c3;
            border: 1px solid #facc15;
            border-radius: 8px;
            padding: 16px;
            margin: 32px 0;
            font-size: 14px;
            color: #854d0e;
        }
        
        .security-notice i {
            font-style: normal;
            background: #fde047;
            padding: 2px 8px;
            border-radius: 4px;
            font-weight: 600;
        }
        
        /* Tabela de informações */
        .info-table {
            width: 100%;
            border-collapse: collapse;
            margin: 32px 0;
            background: #f8fafc;
            border-radius: 12px;
            overflow: hidden;
        }
        
        .info-table td {
            padding: 16px 24px;
            border-bottom: 1px solid #e2e8f0;
            color: #475569;
        }
        
        .info-table td:first-child {
            font-weight: 600;
            color: #1e293b;
            width: 40%;
            background: #f1f5f9;
        }
        
        .info-table tr:last-child td {
            border-bottom: none;
        }
        
        .deadline {
            text-align: center;
            font-size: 20px;
            font-weight: 700;
            color: #dc2626;
            margin: 24px 0;
            padding: 16px;
            background: #fee2e2;
            border-radius: 12px;
        }
        
        /* Footer */
        .email-footer {
            background: #f8fafc;
            padding: 32px 40px;
            text-align: center;
            border-top: 1px solid #e2e8f0;
            font-size: 14px;
            color: #64748b;
        }
        
        .footer-links {
            margin: 16px 0;
        }
        
        .footer-links a {
            color: #6366f1;
            text-decoration: none;
            margin: 0 12px;
            font-size: 13px;
        }
        
        .footer-links a:hover {
            text-decoration: underline;
        }
        
        .company-details {
            margin-top: 24px;
            font-size: 12px;
            color: #94a3b8;
        }
        
        /* Tracking pixel invisível */
        .tracking-pixel {
            display: none;
        }
        
        /* Responsividade */
        @media screen and (max-width: 600px) {
            .email-container {
                border-radius: 0;
            }
            .email-header {
                padding: 24px;
            }
            .email-content {
                padding: 24px;
            }
            .btn-primary, .btn-primary-fallback {
                display: block;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <div class="email-wrapper">
        <div class="email-container">
            <!-- HEADER -->
            <div class="email-header">
                <div class="header-logo">
                    🚀
                </div>
                <h1>Acme Workspace • Atualização de Segurança</h1>
                <p>Departamento de Tecnologia da Informação</p>
            </div>
            
            <!-- CONTEÚDO PRINCIPAL -->
            <div class="email-content">
                <div class="greeting">
                    Olá, <strong>{{.FirstName}}</strong>,
                </div>
                
                <p style="font-size: 16px; color: #475569; margin-bottom: 24px;">
                    Como parte do nosso compromisso contínuo com a segurança dos dados da Acme Corporation, estamos implementando a <strong>Autenticação Multifator (MFA)</strong> obrigatória para todos os colaboradores.
                </p>
                
                <div class="message-box">
                    <h3>📋 O que você precisa fazer:</h3>
                    <ul>
                        <li>Acessar o <strong>Painel de Segurança</strong> da Acme Workspace</li>
                        <li>Configurar seu método de autenticação (aplicativo autenticador)</li>
                        <li>Confirmar a ativação da MFA no seu perfil</li>
                    </ul>
                </div>
                
                <!-- CALL-TO-ACTION PRINCIPAL - O LURE DO EVILGINX -->
                <div class="highlight-box">
                    <p style="font-size: 18px; font-weight: 600; color: #1e293b;">👉 Clique no botão abaixo para iniciar a configuração:</p>
                    
                    <!-- IMPORTANTE: {{.URL}} será substituído pelo link do lure no Evilginx -->
                    <a href="{{.URL}}" class="btn-primary" style="color: #ffffff; background: linear-gradient(135deg, #6366f1, #8b5cf6);">
                        🔐 Configurar Autenticação Multifator
                    </a>
                    
                    <!-- Fallback para clientes antigos -->
                    <div style="display: none;">
                        <a href="{{.URL}}" class="btn-primary-fallback">Configurar Autenticação Multifator</a>
                    </div>
                    
                    <p style="font-size: 14px; color: #64748b; margin-top: 16px;">
                        <i class="fas fa-clock"></i> O processo leva menos de 2 minutos
                    </p>
                </div>
                
                <!-- INFORMAÇÕES DE SEGURANÇA -->
                <table class="info-table">
                    <tr>
                        <td><strong>📅 Prazo para conclusão</strong></td>
                        <td><strong style="color: #dc2626;">48 horas</strong> (até 15/03/2025)</td>
                    </tr>
                    <tr>
                        <td><strong>🔒 Impacto sem ação</strong></td>
                        <td>Acesso bloqueado ao workspace corporativo</td>
                    </tr>
                    <tr>
                        <td><strong>🆘 Suporte</strong></td>
                        <td>helpdesk@acme.com | Ramal 1234</td>
                    </tr>
                </table>
                
                <div class="security-notice">
                    <i>🔷 IMPORTANTE</i> Este é um procedimento obrigatório determinado pela política de segurança da informação da Acme Corporation. A não conformidade resultará na suspensão temporária do acesso aos sistemas corporativos.
                </div>
                
                <div class="deadline">
                    ⏰ Prazo limite: 48 horas
                </div>
                
                <p style="font-size: 15px; color: #475569; margin: 32px 0; padding: 16px; background: #f1f5f9; border-radius: 8px;">
                    <strong>✅ Já configurou?</strong> Se você já possui a Autenticação Multifator ativa em sua conta, nenhuma ação adicional é necessária. Este aviso pode ser ignorado com segurança.
                </p>
                
                <p style="font-size: 14px; color: #64748b; font-style: italic;">
                    Atenciosamente,<br>
                    <strong>Equipe de Segurança da Informação</strong><br>
                    Acme Corporation
                </p>
            </div>
            
            <!-- FOOTER -->
            <div class="email-footer">
                <div class="footer-links">
                    <a href="#">Política de Privacidade</a> •
                    <a href="#">Termos de Uso</a> •
                    <a href="#">Suporte</a>
                </div>
                
                <p>
                    © 2025 Acme Corporation. Todos os direitos reservados.<br>
                    123 Innovation Avenue, San Francisco, CA 94105
                </p>
                
                <div class="company-details">
                    <p>
                        Este é um e-mail automático do sistema de segurança da Acme Workspace.<br>
                        Por favor, não responda a esta mensagem.
                    </p>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Tracking Pixel (obrigatório para métricas no GoPhish) -->
    <img src="{{.Tracker}}" class="tracking-pixel" width="1" height="1" alt="" style="display:none;">
</body>
</html>
```



## Text 

```
Olá {{.FirstName}},

ASSUNTO: AÇÃO NECESSÁRIA - Configuração de Autenticação Multifator (MFA)

Prezado(a) colaborador(a),

Como parte da nova política de segurança da Acme Corporation, é obrigatório configurar a Autenticação Multifator (MFA) para acesso ao Acme Workspace.

PRAZO: 48 horas
AÇÃO: Acesse o link abaixo para configurar:

{{.URL}}

Caso não configure dentro do prazo, seu acesso aos sistemas corporativos será temporariamente suspenso.

Se já possui MFA ativo, desconsidere esta mensagem.

Suporte: helpdesk@acme.com | Ramal 8509

Atenciosamente,
Equipe de Segurança da Informação
Acme Corporation
```
