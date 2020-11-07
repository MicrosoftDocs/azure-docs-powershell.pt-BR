---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945676"
---
# Get-AzureAccount

## Sinopse
Obtém contas do Azure que estão disponíveis para o PowerShell do Azure.

## SYNTAX

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureAccount** Obtém as contas do Azure que estão disponíveis para o Windows PowerShell.
Para disponibilizar suas contas para o Windows PowerShell, use os cmdlets **Add-AzureAccount** ou **Import-PublishSettingsFile** .

## EXEMPLOS

### Exemplo 1: obter todas as contas
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

Esse comando obtém todas as contas associadas ao usuário especificado.

### Exemplo 2: obter uma conta por nome
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

Esse comando obtém a conta ContosoAdmin.

## OS

### -Nome
Obtém apenas a conta especificada.
O padrão é todas as contas que estão disponíveis para o Windows PowerShell.
Digite o nome da conta.
O valor do **nome** diferencia maiúsculas de minúsculas.
Caracteres curinga não são permitidos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Não é possível canalizar a entrada para este cmdlet.

## EXIBE

### Nenhuma
Esse cmdlet não retorna nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


