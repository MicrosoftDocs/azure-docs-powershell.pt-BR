---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427802"
---
# Get-AzureRmADSpCredential

## Sinopse
Recupera uma lista de credenciais associadas a uma entidade de serviço.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ObjectIdParameterSet (padrão)
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmADSpCredential pode ser usado para recuperar uma lista de credenciais associadas a uma entidade de serviço.
Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associados à entidade de serviço.

## EXEMPLOS

### --------------------------Exemplo 1--------------------------
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

Retorna uma lista de credenciais associadas à entidade de serviço com SPN ' http://test12345 '.

## OS

### -ObjectId
A ID de objeto da entidade de serviço para a qual recuperar as credenciais.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceprincipalnamename
O nome (SPN) da entidade de serviço para a qual recuperar as credenciais.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Remove-AzureRmADSpCredential](./Remove-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

