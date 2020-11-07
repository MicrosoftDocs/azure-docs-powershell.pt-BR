---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946198"
---
# New-AzureVMImageDiskConfigSet

## Sinopse
Cria um objeto do conjunto de configuração de disco.

## SYNTAX

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureVMImageDiskConfigSet** cria um objeto do conjunto de configuração de disco que é passado para o cmdlet de atualização de imagem.
Ele encapsula o OSDiskConfig e o objeto DataDiskConfig.
Use os cmdlets **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** para definir as propriedades do disco do sistema operacional e do disco de dados para a imagem da máquina virtual.

## EXEMPLOS

### Exemplo 1: criar um objeto do conjunto de configuração de disco
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

Esse comando cria um objeto do conjunto de configuração de disco e armazena os resultados na variável chamada $Disk.
Após a criação da configuração do disco, ele é usado para definir o OSDiskConfig e o DataDiskConfig.
Em seguida, a máquina virtual é atualizada com a configuração.

## OS

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet

## INFORMA

## LINKS RELACIONADOS

[Get-AzureVMImageDiskConfigSet](./Get-AzureVMImageDiskConfigSet.md)

[Set-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Set-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


