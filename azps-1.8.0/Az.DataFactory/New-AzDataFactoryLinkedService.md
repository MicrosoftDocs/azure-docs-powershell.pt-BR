---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: df5402709de5b16d5bb108dba7bd78d90a00efec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771030"
---
# New-AzDataFactoryLinkedService

## Sinopse
Vincula um repositório de dados ou um serviço na nuvem a uma fábrica de dados do Azure.

## SYNTAX

### ByFactoryName (padrão)
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzDataFactoryLinkedService** vincula um repositório de dados ou um serviço na nuvem ao Azure data Factory.
Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.
Se você especificar o parâmetro *Force* , o cmdlet substituirá o serviço vinculado existente sem confirmação.
Execute estas operações na seguinte ordem: 
- Criar uma fábrica de dados. 
- Criar serviços vinculados. 
- Criar conjuntos de valores de valores. 
- Crie um pipeline.

## EXEMPLOS

### Exemplo 1: criar um serviço vinculado
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamado WikiADF.
Esse serviço vinculado vincula um repositório de blob do Azure especificado no arquivo ao data Factory chamado WikiADF.
O comando passa o resultado para o cmdlet Format-List usando o operador pipeline.
Esse cmdlet do Windows PowerShell formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

## OS

### -Datafactory
Especifica um objeto **PSDataFactory** .
Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Arquivo
Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do serviço vinculado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet substitui um serviço vinculado existente sem solicitar confirmação.

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
Parameter Sets: (All)
Aliases:

Required: False
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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## EXIBE

### Microsoft. Azure. Commands. datafactorings. Models. PSLinkedService

## INFORMA
* Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[Get-AzDataFactoryLinkedService](./Get-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


