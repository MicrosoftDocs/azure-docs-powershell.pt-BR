---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259756"
---
# Remove-AzKustoDatabasePrincipal

## Sinopse
Remover as permissões de entidades de segurança do banco de dados.

## SYNTAX

### RemoveExpanded (padrão)
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### RemoveViaIdentityExpanded
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Remover as permissões de entidades de segurança do banco de dados.

## EXEMPLOS

### Exemplo 1: remover as permissões dos objetos de banco de dados
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

O comando acima remove as permissões de entidades de segurança do banco de dados

## OS

### -ClusterName
O nome do cluster Kusto.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
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
Parameter Sets: RemoveExpanded
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
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o cluster Kusto.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
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
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valor
A lista de objetos Kusto do banco de dados.
Para construir, consulte a seção observações para propriedades de valor e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabasePrincipal

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

VALOR <IDatabasePrincipal [] >: a lista de objetos de banco de dados do Kusto.
  - `Name <String>`: Nome do banco de dados principal.
  - `Role <DatabasePrincipalRole>`: Função de entidade do banco de dados.
  - `Type <DatabasePrincipalType>`: Tipo de entidade de segurança do banco de dados.
  - `[AppId <String>]`: ID do aplicativo-relevante somente para o tipo principal do aplicativo.
  - `[Email <String>]`: Email principal do banco de dados se existe.
  - `[Fqn <String>]`: Nome totalmente qualificado do banco de dados principal.

## LINKS RELACIONADOS

