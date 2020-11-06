---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 47cbd81fa7e2e8f3877c2e933254cde4e2cee8ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426379"
---
# Set-AzureRmDataFactoryV2LinkedService

## Sinopse
Vincula um repositório de dados ou um serviço na nuvem ao data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByFactoryName (padrão)
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceId
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Set-AzureRmDataFactoryV2LinkedService vincula um repositório de dados ou um serviço na nuvem ao Azure data Factory.
Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.
Se você especificar o parâmetro Force, o cmdlet substituirá o serviço vinculado existente sem confirmação.
Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.
--Criar serviços vinculados.
--Criar conjuntos de valores.
--Criar um pipeline.

## EXEMPLOS

### Exemplo 1: criar um serviço vinculado
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamado WikiADF.
Esse serviço vinculado vincula um repositório de blob do Azure especificado no arquivo ao data Factory chamado WikiADF.
O comando passa o resultado para o cmdlet Format-List usando o operador pipeline.
Esse cmdlet do Windows PowerShell formata os resultados.
Para obter mais informações, digite Get-Help formato-List.

## OS

### -Datafactoryname
Especifica o nome de uma fábrica de dados.
Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionFile
O caminho do arquivo JSON.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Executa o cmdlet sem solicitar confirmação.

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

### -Nome
Especifica o nome do serviço vinculado a ser criado.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Esse cmdlet cria um serviço vinculado para o grupo que esse parâmetro especifica.

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

### -ResourceId
A ID do recurso do Azure.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### System. String

## EXIBE

### Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService

## INFORMA
Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[Get-AzureRmDataFactoryV2LinkedService]()

[Remove-AzureRmDataFactoryV2LinkedService]()
