---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888412"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection verifica a conectividade de nós em cluster local para os serviços do Azure exigidos pelo Azure Stack HCI.

## SINTAXE

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## DESCRIPTION
Test-AzStackHCIConnection verifica a conectividade de nós em cluster local para os serviços do Azure exigidos pelo Azure Stack HCI.

## EXEMPLOS

### EXEMPLO 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Invocando um dos nós do cluster. Caso de sucesso.

### EXEMPLO 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Invocando um dos nós do cluster. Caso com falha.

## PARÂMETROS

### -ComputerName
Especifica um dos nós de cluster no cluster local que está sendo registrado no Azure.

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

### -Credential
Especifica a credencial do ComputerName.
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

### -EnvironmentName
Especifica o Ambiente do Azure.
O padrão é o AzureCloud.
Os valores válidos são AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

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

### -Region
Especifica a região à que se conectar.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### PSCustomObject. Retorna propriedades a seguir em PSCustomObject
### Teste: nome do teste executado.
### EndpointTested: Ponto de extremidade usado no teste.
### IsRequired: True ou False
### Resultado: bem-sucedido ou com falha
### FailedNodes: lista de nós nos quais o teste falhou.
## NOTES

## LINKS RELACIONADOS
