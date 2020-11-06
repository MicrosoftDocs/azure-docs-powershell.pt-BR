---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425840"
---
# Get-AzureRmTenant

## Sinopse
Obtém locatários autorizados para o usuário atual.

## SYNTAX

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmTenant Obtém locatários autorizados para o usuário atual.

## EXEMPLOS

### Exemplo 1: obtendo todos os locatários
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

Este exemplo mostra como obter todos os locatários autorizados de uma conta do Azure.

### Exemplo 2: obtendo um locatário específico
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

Este exemplo mostra como obter um locatário autorizado específico de uma conta do Azure.

## OS

### -Tenantid
Especifica a ID do locatário que este cmdlet obtém.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### PSAzureTenant
Esse cmdlet retorna a ID do locatário e as informações de domínio associadas para locatários autorizados para a conta atual.

## INFORMA

## LINKS RELACIONADOS

