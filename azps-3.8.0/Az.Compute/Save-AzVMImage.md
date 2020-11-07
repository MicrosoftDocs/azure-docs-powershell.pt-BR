---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942087"
---
# Save-AzVMImage

## Sinopse
Salva uma máquina virtual como uma VMImage.

## SYNTAX

### ResourceGroupNameParameterSetName (padrão)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Save-AzVMImage** salva uma máquina virtual como uma VMImage.
Antes de criar uma imagem de máquina virtual, Sysprep a máquina virtual e marcá-la como generalizada usando o cmdlet Set-AzVM.
A saída desse cmdlet é um modelo JSON (JavaScript Object Notation).
Você pode implantar máquinas virtuais a partir da sua imagem capturada.

## EXEMPLOS

### Exemplo 1: capturar uma máquina virtual
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

O primeiro comando marca a máquina virtual chamada VirtualMachine07 como generalizada.
O segundo comando captura uma máquina virtual nomeada VirtualMachine07 como uma VMImage.
A propriedade **output** retorna um modelo JSON.

## OS

### -AsJob
Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DestinationContainerName
Especifica o nome de um contêiner dentro do contêiner "sistema" no qual você deseja armazenar as imagens.
Se o contêiner não existir, ele será criado para você.
Os VHDs (discos rígidos virtuais) que constituem a VMImage residem no contêiner que esse parâmetro especifica.
Se os VHDs estiverem espalhados em várias contas de armazenamento, esse cmdlet cria um contêiner que tem esse nome em cada conta de armazenamento.
A URL da imagem salva é semelhante a: https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Especifica a ID do recurso da máquina virtual.

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Substituir
Indica que esse cmdlet substitui todos os VHDs que têm o mesmo prefixo no contêiner de destino.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
O caminho do arquivo no qual o modelo da imagem capturada está armazenado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
Especifica o prefixo no nome dos BLOBs que constituem o perfil de armazenamento da VMImage.
Por exemplo, um prefixo vhdPrefix para um disco do sistema operacional resulta no nome vhdPrefix-OSDisk. \< GUID \> . vhd.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation

## INFORMA

## LINKS RELACIONADOS

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


