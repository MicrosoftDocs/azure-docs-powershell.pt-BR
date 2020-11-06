---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601776"
---
# Get-AzsNetworkAdminOverview

## Sinopse
Obtenha uma visão geral do estado do provedor de recursos de rede.

## SYNTAX

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## DESCRITIVO
Obtenha uma visão geral do estado do provedor de recursos de rede. As propriedades individuais fornecem contas detalhadas de uso de recursos e integridade por componente.

## EXEMPLOS

### --------------------------EXEMPLO 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Obter visão geral do administrador de rede.

### --------------------------EXEMPLO 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Obter o uso do endereço IP público.

## OS

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## INFORMA

## LINKS RELACIONADOS

