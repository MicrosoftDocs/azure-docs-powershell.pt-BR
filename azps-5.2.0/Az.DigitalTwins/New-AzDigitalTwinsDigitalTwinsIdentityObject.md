---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260546"
---
# New-AzDigitalTwinsDigitalTwinsIdentityObject

## Sinopse
Criar um objeto de memória para DigitalTwinsIdentity

## SYNTAX

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## DESCRITIVO
Criar um objeto de memória para DigitalTwinsIdentity

## EXEMPLOS

### Exemplo 1: criar um DigitalTwinsIdentityObject
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

Criar um DigitalTwinsIdentityObject por ID e local

## OS

### -EndpointName
Nome do recurso de ponto de extremidade.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Caminho de identidade do recurso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Local do DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
O nome do DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
O identificador de assinatura.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

### Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. DigitalTwinsIdentity

## INFORMA

ALIASES

## LINKS RELACIONADOS

