---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: dc13bdaf737985f6769b3bb326201100204c6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428731"
---
# Remove-AzureRmSqlServerDnsAlias

## Sinopse
Remove o alias do DNS do SQL Server do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Remover um alias de DNS de servidor de parâmetros de entrada de cmdlet
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Remover um alias DNS de servidor da definição de instância AzureSqlServerDnsAliasModel
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Remover um alias de DNS de servidor de uma ID de recurso do Azure
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Esses comandos removem o alias do DNS do SQL Server do Azure do servidor deixando o servidor intacto.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

Remove o alias DNS do SQL Server do Azure com o nome aliasname do servidor com o nome nomedoservidor

## OS

### -AsJob
Executar o cmdlet em segundo plano
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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ignorar a mensagem de confirmação para executar a ação

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

### -InputObject
O objeto de alias de DNS do servidor a ser removido

```yaml
Type: AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do alias DNS do SQL Server do Azure

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso do objeto de alias DNS do servidor a ser removido

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
O nome do SQL Server do Azure.

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String
Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel

## EXIBE

### Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel

## INFORMA

## LINKS RELACIONADOS
