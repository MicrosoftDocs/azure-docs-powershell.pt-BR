---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264204"
---
# Test-AzKustoDataConnectionNameAvailability

## Sinopse
Verifica se o nome da conexão de dados é válido e ainda não está em uso.

## SYNTAX

### CheckExpanded (padrão)
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentityExpanded
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Verifica se o nome da conexão de dados é válido e ainda não está em uso.

## EXEMPLOS

### Exemplo 1: verificar a disponibilidade de um nome de conexão de dados que está em uso
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

O comando acima retorna se uma conexão de dados chamada "mykustodataconnection" existe ou não no banco de dados "mykustodatabase".

### Exemplo 2: verificar a disponibilidade de um nome de conexão de dados que não está em uso
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

O comando acima retorna se uma conexão de dados chamada "mydataconnection" existe ou não no banco de dados "mykustodatabase".

## OS

### -ClusterName
O nome do cluster Kusto.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
O nome do banco de dados no cluster Kusto.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome da conexão de dados.

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

### -ResourceGroupName
O nome do grupo de recursos que contém o cluster Kusto.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura forma a parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
O tipo de recurso, Microsoft. Kusto/clusters/bancos de dados/conexões de dados.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICheckNameResult

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <IKustoIdentity> : parâmetro de identidade
  - `[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.
  - `[ClusterName <String>]`: O nome do cluster Kusto.
  - `[DataConnectionName <String>]`: O nome da conexão de dados.
  - `[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[Location <String>]`: Local do Azure.
  - `[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.
  - `[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.
  - `[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.

## LINKS RELACIONADOS

