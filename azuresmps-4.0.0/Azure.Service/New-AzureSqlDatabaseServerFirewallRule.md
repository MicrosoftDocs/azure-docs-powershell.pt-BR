---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945969"
---
# New-AzureSqlDatabaseServerFirewallRule

## Sinopse
Cria uma regra de firewall no servidor de banco de dados SQL do Azure.

## SYNTAX

### IpRange (padrão)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSqlDatabaseServerFirewallRule** cria uma regra de firewall na instância especificada do servidor de banco de dados SQL do Azure na assinatura atual.

Use os parâmetros *StartIpAddress* e *endipaddress* para especificar um intervalo de endereços IP que essa regra permite para se conectar ao servidor de banco de dados SQL do Azure.

Especifique o parâmetro *AllowAllAzureServices* para criar uma regra que permita a conexão do Azure com o servidor.
A regra tem valores de endereço IP inicial e final de 0.0.0.0.
Se você não especificar um nome de regra de firewall, esse cmdlet atribuirá o nome padrão AllowAllAzureServices.

## EXEMPLOS

### Exemplo 1: criar uma regra de firewall
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

Esse comando cria uma regra de firewall FirewallRule24 no servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.
O comando especifica um intervalo de endereços IP.

### Exemplo 2: criar uma regra que permita todos os serviços do Azure
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

Esse comando cria uma regra de firewall chamada AzureConnections no servidor chamado lpqd0zbr8y que permite conexões do Azure.

### Exemplo 3: criar uma regra que permita que todos os serviços do Azure que usam o nome padrão criem uma regra que permita todos os serviços do Azure que usam o nome padrão
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

Esse comando cria uma regra de firewall no servidor especificado chamado lpqd0zbr8y, que permite conexões do Azure.
O comando atribui o nome de regra padrão AllowAllAzureServices.

## OS

### -AllowAllAzureServices
Indica que essa regra de firewall permite que todos os endereços IP do Azure acessem o servidor.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endipaddress
Especifica o valor final do intervalo de endereços IP para esta regra.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleName
Especifica o nome da nova regra de firewall.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome de um servidor.
Esse cmdlet cria uma regra de firewall no servidor que esse cmdlet especifica.
Especifique o nome do servidor, não o nome DNS totalmente qualificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartIpAddress
Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext

## INFORMA

## LINKS RELACIONADOS

[Banco de dados SQL do Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Criar regra de firewall](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Operações para bancos de dados SQL do Azure](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


