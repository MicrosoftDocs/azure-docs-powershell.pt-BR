---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892523"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Baixa arquivos de log do processamento HDInsight do Azure.

## SINTAXE

### ByFactoryName (Padrão)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Save-AzDataFactoryLog** baixa arquivos de log associados ao processamento HDInsight do Azure de projetos De Porquinho ou Hive ou para atividades personalizadas no disco rígido local.
Primeiro, execute o cmdlet Get-AzDataFactoryRun para obter uma ID de uma atividade em uma fatia de dados e, em seguida, use essa ID para recuperar arquivos de log do armazenamento blob (objeto grande binário) associado ao cluster HDInsight.
Se você não especificar o parâmetro *DownloadLogs,* o cmdlet retornará apenas o local dos arquivos de log.
Se você especificar *DownloadLogs* sem especificar um diretório de saída (*parâmetro Output),* os arquivos de log serão baixados para a pasta Documentos padrão.
Se você especificar *DownloadLogs* juntamente com uma pasta de saída (*Saída*), os arquivos de log serão baixados para a pasta especificada.

## EXEMPLOS

### Exemplo 1: Salvar arquivos de log em uma pasta específica
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Este comando salva arquivos de log para a atividade executado com a ID de 841b77c9-d56c-48d1-99a3-8c16c3e777d39 onde a atividade pertence a um pipeline no fábrica de dados chamado LogProcessingFactory no grupo de recursos chamado ADF.
Os arquivos de log são salvos na pasta C:\Test.

### Exemplo 2: Salvar arquivos de log na pasta Documentos padrão
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Este comando salva arquivos de log na pasta Documentos (padrão).

### Exemplo 3: Obter o local dos arquivos de log
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Este comando retorna o local dos arquivos de log.
Observe que *DownloadLogs* não é especificado.

## PARÂMETROS

### -DataFactory
Especifica um **objeto PSDataFactory.**

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Especifica o nome de uma fábrica de dados.
Este cmdlet baixa arquivos de log para o fábrica de dados especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -DownloadLogs
Indica que esse cmdlet baixa arquivos de log no computador local.
Se *a pasta* Saída não for especificada, os arquivos serão salvos na pasta Documentos em uma subpasta.

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

### -Id
Especifica a ID da atividade executado para a fatia de dados.
Use o cmdlet Get-AzDataFactoryRun para obter uma ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Output
Especifica a pasta de saída na qual os arquivos de log baixados são salvos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Este cmdlet cria um fábrica de dados que pertence ao grupo especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


