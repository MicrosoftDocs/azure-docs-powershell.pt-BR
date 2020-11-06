---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: be43e56b8106cfde357f1a6c8609cee497158308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430897"
---
# <span data-ttu-id="a979f-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="a979f-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="a979f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a979f-102">SYNOPSIS</span></span>
<span data-ttu-id="a979f-103">Cria propriedades de serviço Web regionais.</span><span class="sxs-lookup"><span data-stu-id="a979f-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a979f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a979f-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a979f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a979f-105">DESCRIPTION</span></span>
<span data-ttu-id="a979f-106">Cria propriedades regionais do Azure Machine Learning para um serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="a979f-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="a979f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a979f-107">EXAMPLES</span></span>

### <span data-ttu-id="a979f-108">Exemplo 1: adicionar novas propriedades regionais para a central oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="a979f-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="a979f-109">Este exemplo de comando cria uma propriedade regional para um serviço Web na região "centro-EUA".</span><span class="sxs-lookup"><span data-stu-id="a979f-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="a979f-110">OS</span><span class="sxs-lookup"><span data-stu-id="a979f-110">PARAMETERS</span></span>

### <span data-ttu-id="a979f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a979f-111">-DefaultProfile</span></span>
<span data-ttu-id="a979f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a979f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a979f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a979f-113">-Force</span></span>
<span data-ttu-id="a979f-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a979f-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a979f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a979f-115">-Name</span></span>
<span data-ttu-id="a979f-116">O nome do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="a979f-116">The name for the web service.</span></span>

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

### <span data-ttu-id="a979f-117">-Região</span><span class="sxs-lookup"><span data-stu-id="a979f-117">-Region</span></span>
<span data-ttu-id="a979f-118">A região na qual criar as propriedades do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="a979f-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="a979f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a979f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a979f-120">O grupo de recursos no qual pertence o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="a979f-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="a979f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a979f-121">-Confirm</span></span>
<span data-ttu-id="a979f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a979f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a979f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a979f-123">-WhatIf</span></span>
<span data-ttu-id="a979f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a979f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a979f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a979f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a979f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a979f-126">CommonParameters</span></span>
<span data-ttu-id="a979f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a979f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a979f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a979f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a979f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a979f-129">INPUTS</span></span>

### <span data-ttu-id="a979f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a979f-130">System.String</span></span>

## <span data-ttu-id="a979f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a979f-131">OUTPUTS</span></span>

### <span data-ttu-id="a979f-132">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="a979f-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="a979f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a979f-133">NOTES</span></span>
<span data-ttu-id="a979f-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a979f-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a979f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a979f-135">RELATED LINKS</span></span>