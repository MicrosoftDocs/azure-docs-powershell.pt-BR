---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 23797a0137b8444e1e7db4d2256ced290ca919f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610302"
---
# New-AzureRmMlWebService

## Sinopse
Cria um novo serviço Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### CreateFromFile
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
Cria um serviço Web do Azure Machine Learning em um grupo de recursos existente.
Se um serviço Web com o mesmo nome existir no grupo de recursos, a chamada funcionará como uma operação de atualização e o serviço Web existente será substituído.

## EXEMPLOS

### Exemplo 1: criar um novo serviço a partir de uma definição baseada em arquivos JSON
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Cria um novo serviço Web do Azure Machine Learning chamado "mywebservicename" no grupo "MyResource Group" e a região do centro sul central do Sul, com base na definição presente no arquivo JSON referenciado.

### Exemplo 2: criar um novo serviço a partir de uma instância do objeto
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Você pode obter uma instância de objeto de serviço Web para personalizar a publicação como um recurso usando o cmdlet Import-AzureRmMlWebService.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
Especifica o caminho para o arquivo que contém a definição de formato JSON do serviço Web.
Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Não peça confirmação.

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

### -Local
A região do serviço Web.
Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".
Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.
O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.
Os grupos de recursos podem conter serviços Web de regiões diferentes.
Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzureRmResourceProvider com o cmdlet de parâmetro ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do serviço Web.
O nome deve ser exclusivo no grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
A definição do novo serviço Web, contendo todas as propriedades que compõem o serviço.
Esse parâmetro é obrigatório e representa uma instância da classe Microsoft. Azure. Management. MachineLearning. WebServices. WebService.
Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos no qual colocar o serviço Web.
Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".
Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.
O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.
Os grupos de recursos podem conter serviços Web de regiões diferentes.
Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzureRmResourceProvider com o cmdlet de parâmetro ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService
Parâmetros: NewWebServiceDefinition (ByValue)

## EXIBE

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService

## INFORMA
Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## LINKS RELACIONADOS
