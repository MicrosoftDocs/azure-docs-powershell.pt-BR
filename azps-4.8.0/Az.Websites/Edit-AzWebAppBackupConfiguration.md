---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 9cf7974cb284052fab0dd6c8cb27409543db272c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114662"
---
# Edit-AzWebAppBackupConfiguration

## Sinopse

## SYNTAX

### FromResourceName
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### FromWebApp
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Edit-AzWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.

## EXEMPLOS

### Exemplo 1

O cmdlet Edit-AzWebAppBackupConfiguration edita o backup de configuração atual para um aplicativo Web do Azure. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Edit-AzWebAppBackupConfiguration -FrequencyInterval <Int32> -FrequencyUnit <String> -KeepAtLeastOneBackup -Name IpRule -ResourceGroupName MyResourceGroup -RetentionPeriodInDays <Int32> -StartTime 2016-11-30T22:00:00Z -StorageAccountUrl 'https://storageaccount.file.core.windows.net'
```

## OS

### -Bancos de dados
Bancos de dados do tipo DatabaseBackupSetting []

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -FrequencyInterval
Intervalo de frequência

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FrequencyUnit
Unidade de frequência

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeepAtLeastOneBackup
Mantenha pelo menos uma opção de backup

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do WebApp

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Período de retenção em dias

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Nome do slot do WebApp

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
StartTime em UTC

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountUrl
URL da conta de armazenamento

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
Objeto WebApp

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. Int32

### System. String

### System. DateTime

### System. Management. Automation. SwitchParameter

### Microsoft. Azure. Commands. webapps. Models. PSSite

### Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting []

## EXIBE

### Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration

## INFORMA

## LINKS RELACIONADOS

[Get-AzWebAppBackupConfiguration](./Get-AzWebAppBackupConfiguration.md)


