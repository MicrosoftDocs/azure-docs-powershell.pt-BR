---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260265"
---
# Test-AzEventHubName

## Sinopse
Verifica a disponibilidade do nome ou alias do NameSpace especificado (nome de configuração DR)

## SYNTAX

### NamespaceCheckNameAvailabilitySet (padrão)
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Test-AzEventhubName** verifica a disponibilidade do nome do namespace ou alias (nome de configuração de Dr)

## EXEMPLOS

### Exemplo 1
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Retorna o status na disponibilidade do nome do namespace ' MyNameSapceName ' como verdadeiro, se disponível

### Exemplo 2
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Retorna o status de disponibilidade do nome do namespace ' MyNameSapceName ' como falso com motivo

### Exemplo 3
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

Retorna o status de disponibilidade do nome do alias ' myaliasname ' para o namespace ' MyNameSapceName ' como verdadeiro, se disponível

## OS

### -Aliasname
Nome de configuração DR-nome do alias

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Nome do namespace do Eventhub

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes

## INFORMA

## LINKS RELACIONADOS
