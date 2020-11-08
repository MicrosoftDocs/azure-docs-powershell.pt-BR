---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124883"
---
# <span data-ttu-id="85795-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="85795-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="85795-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85795-102">SYNOPSIS</span></span>
<span data-ttu-id="85795-103">Cria propriedades de serviço Web regionais.</span><span class="sxs-lookup"><span data-stu-id="85795-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="85795-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85795-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85795-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85795-105">DESCRIPTION</span></span>
<span data-ttu-id="85795-106">Cria propriedades regionais do Azure Machine Learning para um serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="85795-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="85795-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85795-107">EXAMPLES</span></span>

### <span data-ttu-id="85795-108">Exemplo 1: adicionar novas propriedades regionais para a central oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="85795-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="85795-109">Este exemplo de comando cria uma propriedade regional para um serviço Web na região "centro-EUA".</span><span class="sxs-lookup"><span data-stu-id="85795-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="85795-110">OS</span><span class="sxs-lookup"><span data-stu-id="85795-110">PARAMETERS</span></span>

### <span data-ttu-id="85795-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85795-111">-DefaultProfile</span></span>
<span data-ttu-id="85795-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="85795-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85795-113">-Force</span><span class="sxs-lookup"><span data-stu-id="85795-113">-Force</span></span>
<span data-ttu-id="85795-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="85795-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="85795-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="85795-115">-Name</span></span>
<span data-ttu-id="85795-116">O nome do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="85795-116">The name for the web service.</span></span>

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

### <span data-ttu-id="85795-117">-Região</span><span class="sxs-lookup"><span data-stu-id="85795-117">-Region</span></span>
<span data-ttu-id="85795-118">A região na qual criar as propriedades do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="85795-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="85795-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85795-119">-ResourceGroupName</span></span>
<span data-ttu-id="85795-120">O grupo de recursos no qual pertence o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="85795-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="85795-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85795-121">-Confirm</span></span>
<span data-ttu-id="85795-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85795-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85795-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85795-123">-WhatIf</span></span>
<span data-ttu-id="85795-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85795-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85795-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85795-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85795-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85795-126">CommonParameters</span></span>
<span data-ttu-id="85795-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85795-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85795-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85795-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85795-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85795-129">INPUTS</span></span>

### <span data-ttu-id="85795-130">System. String</span><span class="sxs-lookup"><span data-stu-id="85795-130">System.String</span></span>

## <span data-ttu-id="85795-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85795-131">OUTPUTS</span></span>

### <span data-ttu-id="85795-132">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="85795-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="85795-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85795-133">NOTES</span></span>
<span data-ttu-id="85795-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="85795-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="85795-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85795-135">RELATED LINKS</span></span>
