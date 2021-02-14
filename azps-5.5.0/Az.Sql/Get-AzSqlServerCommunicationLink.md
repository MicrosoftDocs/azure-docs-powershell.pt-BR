---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110943"
---
# Get-AzSqlServerCommunicationLink

## Sinopse
Obtém links de comunicação para transações de banco de dados elásticas entre servidores de banco de dados.

## Sintaxe

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzSqlServerCommunicationLink** obtém links de comunicação de servidor para servidor para transações de banco de dados elásticas no Banco de Dados SQL do Azure.
Especifique o nome de um link de comunicação do servidor para ver as propriedades desse link.

## Exemplos

### Exemplo 1: Obter todos os links de comunicação para um servidor
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

Esse comando obtém todos os links de comunicação de servidor para servidor para transações de banco de dados elásticas para o servidor chamado ContosoServer17.

### Exemplo 2: Obter um link de comunicação específico para um servidor
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

Esse comando obtém o link de comunicação servidor para servidor chamado Link01.

### Exemplo 3: Obter todos os links de comunicação para um servidor usando filtragem
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

Esse comando obtém todos os links de comunicação de servidor para servidor para transações de banco de dados elásticas para o servidor chamado ContosoServer17 que começam com "Link".

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinkName
Especifica o nome do link de comunicação do servidor que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Especifica o nome de um servidor.
Este servidor contém um link de comunicação que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel

## Notas
* Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql

## LINKS RELACIONADOS

[New-AzSqlServerCommunicationLink](./New-AzSqlServerCommunicationLink.md)

[Remove-AzSqlServerCommunicationLink](./Remove-AzSqlServerCommunicationLink.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
