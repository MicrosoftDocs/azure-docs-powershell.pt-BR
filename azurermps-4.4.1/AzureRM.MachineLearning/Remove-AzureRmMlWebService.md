---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432202"
---
# <span data-ttu-id="86fd6-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="86fd6-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="86fd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="86fd6-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="86fd6-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86fd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86fd6-104">SYNTAX</span></span>

### <span data-ttu-id="86fd6-105">Remover um recurso do serviço Web do Azure ML por nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86fd6-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86fd6-106">Remover um serviço Web do Azure ML especificado como um objeto.</span><span class="sxs-lookup"><span data-stu-id="86fd6-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86fd6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86fd6-107">DESCRIPTION</span></span>
<span data-ttu-id="86fd6-108">Exclui um serviço Web do Azure Machine Learning referenciado pelo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86fd6-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="86fd6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86fd6-109">EXAMPLES</span></span>

### <span data-ttu-id="86fd6-110">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="86fd6-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="86fd6-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="86fd6-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="86fd6-112">OS</span><span class="sxs-lookup"><span data-stu-id="86fd6-112">PARAMETERS</span></span>

### <span data-ttu-id="86fd6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="86fd6-113">-Force</span></span>
<span data-ttu-id="86fd6-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="86fd6-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86fd6-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="86fd6-115">-MlWebService</span></span>
<span data-ttu-id="86fd6-116">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="86fd6-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86fd6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="86fd6-117">-Name</span></span>
<span data-ttu-id="86fd6-118">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="86fd6-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86fd6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86fd6-119">-ResourceGroupName</span></span>
<span data-ttu-id="86fd6-120">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="86fd6-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86fd6-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86fd6-121">-Confirm</span></span>
<span data-ttu-id="86fd6-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86fd6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86fd6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86fd6-123">-WhatIf</span></span>
<span data-ttu-id="86fd6-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86fd6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86fd6-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86fd6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86fd6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fd6-126">-DefaultProfile</span></span>
<span data-ttu-id="86fd6-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86fd6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86fd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fd6-128">CommonParameters</span></span>
<span data-ttu-id="86fd6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86fd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fd6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86fd6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fd6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86fd6-131">INPUTS</span></span>

### <span data-ttu-id="86fd6-132">Serviço</span><span class="sxs-lookup"><span data-stu-id="86fd6-132">WebService</span></span>
<span data-ttu-id="86fd6-133">O parâmetro ' MlWebService ' aceita o valor do tipo ' WebService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="86fd6-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="86fd6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86fd6-134">OUTPUTS</span></span>

### <span data-ttu-id="86fd6-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="86fd6-135">None</span></span>

## <span data-ttu-id="86fd6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86fd6-136">NOTES</span></span>
<span data-ttu-id="86fd6-137">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="86fd6-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="86fd6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86fd6-138">RELATED LINKS</span></span>

