---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427666"
---
# Get-AzureRmEnrollmentAccount

## Sinopse
Obter contas de registro.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Lista (padrão)
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Apenas
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmEnrollmentAccount** Obtém contas de registro.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

Obter todas as contas de registro disponíveis.

### Exemplo 2
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

Obter a conta de registro com a ID de objeto especificada.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
ObjectId de uma conta de Registro específica a ser obtida.

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. billing. Models. PSEnrollmentAccount, Microsoft. Azure. Commands. Billing, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. billing. Models. PSEnrollmentAccount

## INFORMA

## LINKS RELACIONADOS

