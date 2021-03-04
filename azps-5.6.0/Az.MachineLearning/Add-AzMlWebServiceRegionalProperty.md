---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885430"
---
# <span data-ttu-id="7e708-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="7e708-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="7e708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e708-102">SYNOPSIS</span></span>
<span data-ttu-id="7e708-103">Cria propriedades de serviço Web regionais.</span><span class="sxs-lookup"><span data-stu-id="7e708-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="7e708-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e708-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e708-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e708-105">DESCRIPTION</span></span>
<span data-ttu-id="7e708-106">Cria propriedades regionais do Azure Machine Learning para um serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="7e708-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="7e708-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e708-107">EXAMPLES</span></span>

### <span data-ttu-id="7e708-108">Exemplo 1: Adicionar novas propriedades regionais para a Central Ocidental dos EUA</span><span class="sxs-lookup"><span data-stu-id="7e708-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="7e708-109">Este comando de exemplo cria uma propriedade regional para um serviço Web na região "West Central US".</span><span class="sxs-lookup"><span data-stu-id="7e708-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="7e708-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e708-110">PARAMETERS</span></span>

### <span data-ttu-id="7e708-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e708-111">-DefaultProfile</span></span>
<span data-ttu-id="7e708-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7e708-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e708-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7e708-113">-Force</span></span>
<span data-ttu-id="7e708-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7e708-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7e708-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e708-115">-Name</span></span>
<span data-ttu-id="7e708-116">O nome do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7e708-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e708-117">-Region</span><span class="sxs-lookup"><span data-stu-id="7e708-117">-Region</span></span>
<span data-ttu-id="7e708-118">A região na qual criar as propriedades do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7e708-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="7e708-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e708-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e708-120">O grupo de recursos no qual o serviço Web pertence.</span><span class="sxs-lookup"><span data-stu-id="7e708-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e708-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e708-121">-Confirm</span></span>
<span data-ttu-id="7e708-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e708-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e708-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e708-123">-WhatIf</span></span>
<span data-ttu-id="7e708-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e708-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e708-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e708-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e708-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e708-126">CommonParameters</span></span>
<span data-ttu-id="7e708-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e708-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e708-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e708-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e708-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e708-129">INPUTS</span></span>

### <span data-ttu-id="7e708-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7e708-130">System.String</span></span>

## <span data-ttu-id="7e708-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e708-131">OUTPUTS</span></span>

### <span data-ttu-id="7e708-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7e708-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7e708-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e708-133">NOTES</span></span>
<span data-ttu-id="7e708-134">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7e708-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7e708-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e708-135">RELATED LINKS</span></span>
