---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261031"
---
# Test-AzStackHCIConnection

## Sinopse
Test-AzStackHCIConnection verifica a conectividade de nós clusterizados locais para os serviços do Azure exigida pela HCI de pilha do Azure.

## SYNTAX

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## DESCRITIVO
Test-AzStackHCIConnection verifica a conectividade de nós clusterizados locais para os serviços do Azure exigida pela HCI de pilha do Azure.

## EXEMPLOS

### EXEMPLO 1
```
Invoking on one of the cluster node. Success case.
```

\>Teste C:\PS-AzStackHCIConnection: conecta-se ao serviço de HCI de pilha do Azure EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: resultado real: êxito

### EXEMPLO 2
```
Invoking on one of the cluster node. Failed case.
```

\>Teste C:\PS-AzStackHCIConnection: conecta-se ao serviço HCI de pilha do Azure EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: resultado verdadeiro: falha FailedNodes: Node1inClus2, Node2inClus3

## OS

### -ComputerName
Especifica um dos nós do cluster no cluster local que está sendo registrado no Azure.

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
Especifica a credencial para o ComputerName.
Padrão é o usuário atual que está executando o cmdlet.

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

### -Environmentname
Especifica o ambiente do Azure.
O padrão é AzureCloud.
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

### -Região
Especifica a região à qual se conectar.
Não usado, a menos que seja Canárias região.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### PSCustomObject. Retorna as propriedades a seguir no PSCustomObject
### Teste: nome do teste executado.
### EndpointTested: ponto de extremidade usado no teste.
### IsRequired: true ou false
### Resultado: êxito ou falha
### FailedNodes: lista de nós em que o teste falhou.
## INFORMA

## LINKS RELACIONADOS
