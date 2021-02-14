---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111283"
---
# Test-AzStackHCIConnection

## Sinopse
Test-AzStackHCIConnection verifica a conectividade de nós clusterados locais para os serviços do Azure exigidos pelo HCI do Azure Stack.

## Sintaxe

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Descrição
Test-AzStackHCIConnection verifica a conectividade de nós clusterados locais para os serviços do Azure exigidos pelo HCI do Azure Stack.

## Exemplos

### EXEMPLO 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Invoking on a of the cluster node. Caso de sucesso.

### EXEMPLO 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Invoking on a of the cluster node. Caso com falha.

## Parâmetros

### -NomedoCompr computador
Especifica um dos nó de cluster no cluster local que está sendo registrado no Azure.

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

### -Credencial
Especifica a credencial para o NomeDoCompt.
O padrão é o usuário atual executando o Cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Região
Especifica a Região à onde se conectar.
Não é usado, a menos que seja região canária.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

## Saídas

### Pscustomobject. Retorna propriedades a seguir no PSCustomObject
### Teste: Nome do teste executado.
### Ponto de Extremidade Testado: Ponto de extremidade usado no teste.
### IsRequired: True or False
### Resultado: Bem-sucedido ou Com Falha
### FailedNodes: Lista de nós em que o teste falhou.
## Notas

## LINKS RELACIONADOS
