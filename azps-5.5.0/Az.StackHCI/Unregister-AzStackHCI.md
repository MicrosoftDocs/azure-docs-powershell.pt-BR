---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e5ff59889b2b786d07699a5b9d46937372c0662f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110883"
---
# Unregister-AzStackHCI

## Sinopse
Unregister-AzStackHCI exclui o recurso de nuvem Microsoft.AzureStackHCI que representa o cluster local e não contata o cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.

## Sintaxe

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
Unregister-AzStackHCI exclui o recurso de nuvem Microsoft.AzureStackHCI que representa o cluster local e não contata o cluster local com o Azure.
As informações registradas disponíveis no cluster são usadas para não registrar o cluster se nenhum parâmetro for passado.

## Exemplos

### EXEMPLO 1
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
Revogar em um dos nó de cluster

### EXEMPLO 2
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
Revogar do nó de gerenciamento

### EXEMPLO 3
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
Revogar do WAC

### EXEMPLO 4
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
Revogar com todos os parâmetros

## Parâmetros

### -AccountId
Especifica o token de acesso ARM.
Especificar isso junto com o ArmAccessToken e o GraphAccessToken evitará o logon interativo do Azure.

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
Especifica o token de acesso ARM.
Especificar isso junto com o GraphAccessToken e o AccountId evitará o logon interativo do Azure.

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

### -NomedoCompr computador
Especifica um dos nó de cluster no cluster local que está sendo registrado no Azure.

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

### -Credencial
Especifica a credencial para o NomeDoCompt.
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

### -Nome do Ambiente
Especifica o Ambiente do Azure.
O padrão é o AzureCloud.
Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSCloudment, AzureGermanCloud, AzurePPE

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
Especifica o token de acesso Graph.
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
Se não especificado \<LocalClusterName\> , -rg será usado como nome do grupo de recursos.

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
Se não especificado, o nome do cluster local será usado.

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
Especifica o Azure TenantId.

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
Use a autenticação de código do dispositivo em vez de um prompt interativo do navegador.

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

## Saídas

### Pscustomobject. Retorna propriedades a seguir no PSCustomObject
### Resultado: Êxito ou Falha ou Cancelamento.
## Notas

## LINKS RELACIONADOS
