---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117192"
---
# Unregister-AzStackHCI

## Sinopse
Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.

## SYNTAX

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Unregister-AzStackHCI exclui o recurso de nuvem Microsoft. AzureStackHCI que representa o cluster local e cancela o registro do cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para cancelar o registro do cluster, caso nenhum parâmetro seja passado.

## EXEMPLOS

### EXEMPLO 1
```
Invoking on one of the cluster node
```

C:\PS \> Unregister-AzStackHCI Result: Success

### EXEMPLO 2
```
Invoking from the management node
```

C:\PS \> Unregister-AzStackHCI-ComputerName ClusterNode1 Result: Success

### EXEMPLO 3
```
Invoking from WAC
```

C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ERE =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -ResourceId DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultado: êxito

### EXEMPLO 4
```
Invoking with all the parameters
```

C:\PS \> Unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ResourceId HciCluster1-tenantid "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ERE =-GraphAccessToken ACEE.. rerrer-AccountId user1@corp1.com -environmentname AzureCloud-ComputerName node1hci-Credential Get-Credential Result: Success

## OS

### -SubscriptionId
Especifica a assinatura do Azure para criar o recurso

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Especifica o nome do recurso do recurso criado no Azure.
Se não for especificado, o nome do cluster local será usado.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantid
Especifica o Tenantid do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos do Azure.
Se não especificado \<LocalClusterName\> -RG será usado como nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Especifica o token de acesso do ARM.
Ao especificar isso, o GraphAccessToken e o AccountId evitarão o logon interativo do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Especifica o token de acesso do gráfico.
Ao especificar isso, o ArmAccessToken e o AccountId evitarão o logon interativo do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Especifica o token de acesso do ARM.
Especificar isso juntamente com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Environmentname
Especifica o ambiente do Azure.
O padrão é AzureCloud.
Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Especifica um dos nós do cluster no cluster local que está sendo registrado no Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Especifica a credencial para o ComputerName.
Padrão é o usuário atual que está executando o cmdlet.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### PSCustomObject. Retorna as propriedades a seguir no PSCustomObject
### Resultado: êxito ou falha ou cancelado.
## INFORMA

## LINKS RELACIONADOS
