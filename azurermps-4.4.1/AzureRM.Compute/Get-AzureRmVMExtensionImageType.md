---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 45accc1c3fd52720d3764a9167f6354316a0c9fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428265"
---
# Get-AzureRmVMExtensionImageType

## Sinopse
Obtém o tipo de uma extensão do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMExtensionImageType** Obtém o tipo de uma extensão do Azure.

## EXEMPLOS

### Exemplo 1: obter um tipo de imagem de extensão
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

Esse comando obtém o tipo de imagem de extensão do Publicador e local especificados.

## OS

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

### -Local
Especifica o local de uma extensão.
Esse cmdlet obtém o tipo de uma extensão no local que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Especifica o nome de um fornecedor de uma extensão.
Para obter um fornecedor de extensão, use o cmdlet Get-AzureRmVMImagePublisher.
Esse cmdlet obtém o tipo de uma extensão do Publicador que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)


