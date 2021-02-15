---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118951"
---
# Invoke-AzKustoDetachClusterFollowerDatabase

## Sinopse
Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.

## Sintaxe

### DetachExpanded (Padrão)
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DetachViaIdentityExpanded
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Descrição
Desconecta todos os seguidores de um banco de dados pertencente a esse cluster.

## Exemplos

### Exemplo 1: Desvincular um banco de dados de seguidores
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

O comando acima desconecta o banco de dados de seguidore definido em AttachedDatabaseConfiguration "myfollowerconfiguration" de cluster "testnewkustoclusterf".

## Parâmetros

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

### -AttachedDatabaseConfigurationName
Nome do recurso da configuração de banco de dados anexada no cluster de seguidores.

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

### -ClusterName
O nome do cluster de Kusto.

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterResourceId
ID do recurso do cluster que segue um banco de dados pertencente a esse cluster.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -InputObject
Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Executar o comando assíncrona

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

### -PassThru
Retorna verdadeiro quando o comando é bem-sucedido

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

### -ResourceGroupName
O nome do grupo de recursos que contém o cluster de Kusto.

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity

## Saídas

### System.Boolean

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade
  - `[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.
  - `[ClusterName <String>]`: o nome do cluster de Kusto.
  - `[DataConnectionName <String>]`: o nome da conexão de dados.
  - `[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.
  - `[Id <String>]`: Caminho de identidade de recursos
  - `[Location <String>]`: local do Azure.
  - `[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.
  - `[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.
  - `[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura faz parte do URI para cada chamada de serviço.

## LINKS RELACIONADOS

