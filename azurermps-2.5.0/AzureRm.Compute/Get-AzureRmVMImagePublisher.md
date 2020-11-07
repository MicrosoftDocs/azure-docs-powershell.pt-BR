---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786185"
---
# Get-AzureRmVMImagePublisher

## Sinopse
Obtém os editores da VMImage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMImagePublisher** Obtém os editores da VMImage.

## EXEMPLOS

### Exemplo 1: obter editores de VMImage para uma região
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

Esse comando obtém os editores de instâncias de VMImage para a região central dos EUA dentro do seu perfil do Azure.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Local
Especifica o local da VMImage.

```yaml
Type: String
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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Save-AzureRmVMImage](./Save-AzureRmVMImage.md)


