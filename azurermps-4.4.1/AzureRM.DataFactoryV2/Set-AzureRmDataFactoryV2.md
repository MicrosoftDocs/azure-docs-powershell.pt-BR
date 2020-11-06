---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441572"
---
# <span data-ttu-id="dd4cd-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd4cd-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="dd4cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4cd-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd4cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd4cd-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="dd4cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd4cd-106">O cmdlet **set-AzureRmDataFactoryV2** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="dd4cd-107">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="dd4cd-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="dd4cd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd4cd-108">EXAMPLES</span></span>

### <span data-ttu-id="dd4cd-109">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="dd4cd-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="dd4cd-110">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="dd4cd-111">OS</span><span class="sxs-lookup"><span data-stu-id="dd4cd-111">PARAMETERS</span></span>

### <span data-ttu-id="dd4cd-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd4cd-112">-Confirm</span></span>
<span data-ttu-id="dd4cd-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4cd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="dd4cd-114">-Force</span></span>
<span data-ttu-id="dd4cd-115">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dd4cd-116">-Local</span><span class="sxs-lookup"><span data-stu-id="dd4cd-116">-Location</span></span>
<span data-ttu-id="dd4cd-117">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd4cd-118">-Name</span></span>
<span data-ttu-id="dd4cd-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd4cd-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="dd4cd-122">-Tag</span></span>
<span data-ttu-id="dd4cd-123">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4cd-124">-WhatIf</span></span>
<span data-ttu-id="dd4cd-125">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4cd-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="dd4cd-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd4cd-126">INPUTS</span></span>

### <span data-ttu-id="dd4cd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4cd-127">System.String</span></span>
<span data-ttu-id="dd4cd-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd4cd-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd4cd-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd4cd-129">OUTPUTS</span></span>

### <span data-ttu-id="dd4cd-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd4cd-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="dd4cd-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd4cd-131">NOTES</span></span>
<span data-ttu-id="dd4cd-132">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="dd4cd-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dd4cd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd4cd-133">RELATED LINKS</span></span>
[<span data-ttu-id="dd4cd-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd4cd-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="dd4cd-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dd4cd-135">Remove-AzureRmDataFactoryV2</span></span>]()
