---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945773"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Sinopse
Inicia a criação de um plano de migração.

## SYNTAX

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** inicia a criação de um plano de migração.
A criação de um plano de migração é assíncrona.
Para ver o status do plano de migração, use o cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .

## EXEMPLOS

### Exemplo 1: iniciar um plano de migração
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Esse comando inicia a criação de um plano de migração para o contêiner herdado chamado OneSDKAzureCloud.
O comando retorna uma mensagem sobre o status do plano e usar o cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** para obter informações atualizadas sobre a data.

### Exemplo 2: iniciar o plano de migração para todos os contêineres de volume
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Esse comando inicia a criação do plano de migração para todos os contêineres de volume herdados no arquivo de configuração que é importado.

## OS

### -Tudo
Indica que esse cmdlet inicia estimativas do tempo de migração para todos os contêineres de volume no arquivo de configuração importado.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Especifica a identificação exclusiva da configuração do aplicativo herdado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyContainerNames
Especifica uma matriz de nomes de contêineres de volume para os quais criar um plano de migração.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### String
Esse cmdlet retornará o status do trabalho do plano de migração se ele tiver sido iniciado com êxito no aplicativo.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


