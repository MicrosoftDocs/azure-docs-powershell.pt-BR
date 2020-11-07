---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946583"
---
# Update-AzureVMImage

## Sinopse
Atualiza o rótulo de uma imagem do sistema operacional no repositório de imagens.

## SYNTAX

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureVMImage** atualiza o rótulo em uma imagem do sistema operacional no repositório de imagens.
Ele retorna um objeto Image com informações sobre a imagem atualizada.

## EXEMPLOS

### Exemplo 1: atualizar uma imagem alterando o rótulo da imagem
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

Esse comando atualiza a imagem chamada Windows-Server-2008-SP2 alterando o rótulo de imagem para DoNotUse.

### Exemplo 2: obter todos os sistemas operacionais por rótulo e atualizar a etiqueta
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

Esse comando obtém todas as imagens do sistema operacional rotuladas DoNotUse e altera o rótulo para atualizado.

## OS

### -Descrição
Especifica a descrição da imagem do sistema operacional.

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

### -DiskConfig
Especifica o disco do sistema operacional e a configuração do disco de dados para a imagem da máquina virtual criada usando cmdlets **New-AzureVMImageDiskConfigSet** , **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** .

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DontShowInGui
Indica que esse cmdlet não mostra a imagem na GUI.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EULA
Especifica o contrato de licença de usuário final.
Recomendamos que o valor seja uma URL.

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

### -Iconname
Especifica o nome do ícone padrão para a imagem do sistema operacional ou da máquina virtual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageFamily
Especifica um valor que pode ser usado para agrupar imagens do sistema operacional ou da máquina virtual.

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

### -ImageName
Especifica o nome da imagem a ser atualizada no repositório de imagens.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Rótulo
Especifica o novo rótulo da imagem.

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

### -Idioma
Especifica o idioma para o sistema operacional na máquina virtual ou na imagem do sistema operacional.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivacyUri
Especifica o URI que aponta para um documento que contém a política de privacidade relacionada à imagem do sistema operacional.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishedDate
Especifica a data em que a imagem do sistema operacional foi adicionada ao repositório de imagens.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecommendedVMSize
Especifica o tamanho da máquina virtual.

Os valores aceitáveis para esse parâmetro são:

- Port
- Muita
- ExtraLarge
- A5
- A6
- A7

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SmallIconname
Especifica o nome do ícone pequeno para a imagem do sistema operacional ou da máquina virtual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### OSImageContext

## INFORMA

## LINKS RELACIONADOS

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[New-AzureVMImageDiskConfigSet](./New-AzureVMImageDiskConfigSet.md)

[Set-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Set-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


