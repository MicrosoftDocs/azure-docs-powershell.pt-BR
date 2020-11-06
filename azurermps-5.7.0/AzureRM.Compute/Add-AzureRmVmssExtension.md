---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426814"
---
# Add-AzureRmVmssExtension

## Sinopse
Adiciona uma extensão ao VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmVmssExtension** adiciona uma extensão ao conjunto de dimensionamento de máquina virtual (VMSS).

## EXEMPLOS

### Exemplo 1: adicionar uma extensão ao VMSS
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

Esse comando adiciona uma extensão ao VMMS.

## OS

### -AutoUpgradeMinorVersion
Indica se a versão de extensão deve ser atualizada automaticamente para uma versão secundária mais recente.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da extensão que este cmdlet adiciona.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtectedSetting
Especifica a configuração particular para a extensão, como uma cadeia de caracteres.
Esse cmdlet criptografa a configuração particular.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Especifica o nome do fornecedor da extensão.
O fornecedor fornece um nome quando o Publicador registra uma extensão.
Isso pode usar o cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) para obter o editor.

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

### -Configuração
Especifica a configuração pública, como uma cadeia de caracteres, para a extensão.
Este cmdlet não criptografa a configuração pública.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de extensão.
Você pode usar o cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) para obter o tipo de extensão.

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

### -TypeHandlerVersion
Especifica a versão da extensão a ser usada para esta máquina virtual.
Você pode usar o cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) para obter a versão da extensão.

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

### -VirtualMachineScaleSet
Especifique o objeto VMSS.
Você pode usar o [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

###  
Esse cmdlet não gera nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmVmssExtension](./Remove-AzureRmVmssExtension.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
