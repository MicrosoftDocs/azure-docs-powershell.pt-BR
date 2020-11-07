---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786556"
---
# Set-AzureRmVMPlan

## Sinopse
Define as informações do plano do Marketplace em uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVMPlan** define as informações de plano do Azure Marketplace para uma máquina virtual.

Antes de poder implantar uma imagem do Marketplace por meio da linha de comando, o acesso programático deve ser habilitado ou a máquina virtual deve ser implantada usando o portal do Azure.

## EXEMPLOS

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

### -Nome
Especifica o nome da imagem do Marketplace.
Esse é o mesmo valor retornado pelo cmdlet Get-AzureRmVMImageSku.
Para obter mais informações sobre como localizar informações sobre a imagem, consulte navegando e selecionando as imagens da máquina virtual do Azure com o PowerShell e a CLI do Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) na documentação do Microsoft Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Produto
Especifica o produto da imagem do Marketplace.
Essas são as mesmas informações do valor **offer** do elemento **imageReference** .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromotionCode
Especifica um código promocional.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Especifica o fornecedor da imagem.
Você pode encontrar essas informações usando o cmdlet Get-AzureRmVMImagePublisher.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual para o qual definir um plano do Marketplace.
Você pode usar o cmdlet Get-AzureRmVM para obter um objeto de máquina virtual.
Você pode usar o cmdlet New-AzureRmVMConfig para criar um objeto de máquina virtual.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSVirtualMachine
O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)
