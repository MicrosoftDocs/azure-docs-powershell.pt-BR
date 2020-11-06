---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: cc6c596b028ca7a4b89083ff06d37b3df9c3ed7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431004"
---
# Import-AzureRmMlWebService

## Sinopse
Importa um objeto JSON para uma definição de serviço Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ImportFromJSONFile
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImportFromJSONString.
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Import-AzureRmMlWebService importa, especificado diretamente ou em um arquivo referenciado, e cria um objeto de definição de serviço Web que pode ser passado para o cmdlet New-AzureRmMlWebService.

## EXEMPLOS

### --------------------------Exemplo 1: importar da cadeia de caracteres--------------------------
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### --------------------------Exemplo 2: importar do caminho do arquivo--------------------------
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
O caminho para o arquivo que contém a definição do serviço Web a ser importado.

```yaml
Type: String
Parameter Sets: ImportFromJSONFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jsonstring
A cadeia de caracteres formatada JSON que contém a definição do serviço Web a ser importada.

```yaml
Type: String
Parameter Sets: ImportFromJSONString.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## INFORMA
Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## LINKS RELACIONADOS

