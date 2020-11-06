---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430452"
---
# <span data-ttu-id="f00cf-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f00cf-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="f00cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f00cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f00cf-103">Exclui um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f00cf-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f00cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f00cf-104">SYNTAX</span></span>

### <span data-ttu-id="f00cf-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f00cf-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00cf-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="f00cf-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00cf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f00cf-107">DESCRIPTION</span></span>
<span data-ttu-id="f00cf-108">Exclui um serviço Web do Azure Machine Learning referenciado pelo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f00cf-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="f00cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f00cf-109">EXAMPLES</span></span>

### <span data-ttu-id="f00cf-110">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f00cf-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="f00cf-111">OS</span><span class="sxs-lookup"><span data-stu-id="f00cf-111">PARAMETERS</span></span>

### <span data-ttu-id="f00cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00cf-112">-DefaultProfile</span></span>
<span data-ttu-id="f00cf-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f00cf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f00cf-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f00cf-114">-Force</span></span>
<span data-ttu-id="f00cf-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f00cf-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f00cf-116">-MlWebService</span></span>
<span data-ttu-id="f00cf-117">O serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f00cf-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f00cf-118">-Name</span></span>
<span data-ttu-id="f00cf-119">O nome do serviço Web a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f00cf-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="f00cf-121">O grupo de recursos do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f00cf-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f00cf-122">-Confirm</span></span>
<span data-ttu-id="f00cf-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f00cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00cf-124">-WhatIf</span></span>
<span data-ttu-id="f00cf-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f00cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f00cf-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f00cf-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00cf-127">CommonParameters</span></span>
<span data-ttu-id="f00cf-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00cf-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00cf-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f00cf-130">INPUTS</span></span>

### <span data-ttu-id="f00cf-131">Serviço</span><span class="sxs-lookup"><span data-stu-id="f00cf-131">WebService</span></span>
<span data-ttu-id="f00cf-132">O parâmetro ' MlWebService ' aceita o valor do tipo ' WebService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f00cf-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f00cf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f00cf-133">OUTPUTS</span></span>

### <span data-ttu-id="f00cf-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f00cf-134">None</span></span>

## <span data-ttu-id="f00cf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f00cf-135">NOTES</span></span>
<span data-ttu-id="f00cf-136">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f00cf-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f00cf-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f00cf-137">RELATED LINKS</span></span>

