---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: 3f38a11cd5d4a124e7db7a99422239f73cbe96dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888411"
---
# Unregister-AzStackHCI

## SYNOPSIS
Unregister-AzStackHCI exclui o recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e não registrou o cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.

## SINTAXE

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Unregister-AzStackHCI exclui o recurso de nuvem do Microsoft.AzureStackHCI que representa o cluster local e não registrou o cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.

## EXEMPLOS

### EXEMPLO 1
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
Invocando em um dos nós de cluster

### EXEMPLO 2
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
Invocando do nó de gerenciamento

### EXEMPLO 3
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
Invocando do WAC

### EXEMPLO 4
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
Invocando com todos os parâmetros

## PARÂMETROS

### -AccountId
Especifica o token de ARM de acesso.
Especificar isso junto com ArmAccessToken e GraphAccessToken evitará o logon interativo do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Especifica o token de ARM de acesso.
Especificar isso junto com GraphAccessToken e AccountId evitará o logon interativo do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Especifica um dos nós de cluster no cluster local que está sendo registrado no Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Especifica a credencial do ComputerName.
O padrão é o usuário atual executando o Cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Especifica o Ambiente do Azure.
O padrão é o AzureCloud.
Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Especifica o token de acesso graph.
Especificar isso junto com ArmAccessToken e AccountId evitará o logon interativo do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do Grupo de Recursos do Azure.
Se não especificado \<LocalClusterName\> -rg será usado como nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Especifica o nome do recurso criado no Azure.
Se não for especificado, o nome do cluster local será usado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Especifica a Assinatura do Azure para criar o recurso

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Especifica o TenantId do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication
Use a autenticação de código de dispositivo em vez de um prompt interativo do navegador.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
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

### PSCustomObject. Retorna propriedades a seguir em PSCustomObject
### Resultado: Êxito ou Falha ou Cancelamento.
## NOTES

## LINKS RELACIONADOS
