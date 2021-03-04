---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887026"
---
# New-AzBlockchainTransactionNode

## SYNOPSIS
Crie ou atualize o nó de transação.

## SINTAXE

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Crie ou atualize o nó de transação.

## EXEMPLOS

### Exemplo 1: Criar um nó de transação de blockchain
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

Este comando cria um nó de transação de bloco de dados.

## PARÂMETROS

### -AsJob
Executar o comando como um trabalho

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlockchainMemberName
Nome de membro da cadeia de dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRule
Obtém ou define as regras de firewall.
Para construir, consulte a seção NOTES para propriedades FIREWALLRULE e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Obtém ou define o local do nó da transação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome do nó de transação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Executar o comando de forma assíncrona

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Define a senha básica do ponto de extremidade dns do nó de transação.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o recurso.
Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


FIREWALLRULE <IFirewallRule[]>: obtém ou define as regras de firewall.
  - `[EndIPAddress <String>]`: Obtém ou define o endereço IP final do intervalo de regras de firewall.
  - `[RuleName <String>]`: Obtém ou define o nome das regras de firewall.
  - `[StartIPAddress <String>]`: Obtém ou define o endereço IP inicial do intervalo de regras de firewall.

## LINKS RELACIONADOS

