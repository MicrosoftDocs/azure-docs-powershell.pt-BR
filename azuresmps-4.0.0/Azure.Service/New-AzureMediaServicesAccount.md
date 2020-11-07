---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945911"
---
# New-AzureMediaServicesAccount

## Sinopse
Cria uma conta do Azure Media Services.

**Observação:** Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## SYNTAX

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **New-AzureMediaServicesAccount** cria uma nova conta de serviços de mídia com o nome da conta de serviços de mídia especificado, o local do Data Center em que você deseja criar a conta e um nome de conta de armazenamento existente.
A conta de armazenamento precisa estar localizada no mesmo Data Center que a nova conta de serviços de mídia.

## EXEMPLOS

### Exemplo 1: criar uma nova conta de serviços de mídia
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## OS

### -Local
Especifica o local do datacenter dos serviços de mídia.

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

### -Nome
Especifica o nome da conta dos serviços de mídia.

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

### -StorageAccountName
Especifica o nome da conta de armazenamento.
A conta de armazenamento já deve existir no mesmo datacenter que a nova conta de serviços de mídia.

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

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Como usar o Azure PowerShell para serviços de mídia](https://go.microsoft.com/fwlink/?LinkId=324179)

[Get-AzureMediaServicesAccount](./Get-AzureMediaServicesAccount.md)

[Remove-AzureMediaServicesAccount](./Remove-AzureMediaServicesAccount.md)


