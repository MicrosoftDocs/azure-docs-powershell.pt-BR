---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426901"
---
# <span data-ttu-id="e61f6-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e61f6-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="e61f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e61f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e61f6-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e61f6-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e61f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e61f6-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e61f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e61f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e61f6-106">O cmdlet **set-AzureRmDataFactoryV2** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="e61f6-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="e61f6-107">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="e61f6-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="e61f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e61f6-108">EXAMPLES</span></span>

### <span data-ttu-id="e61f6-109">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="e61f6-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="e61f6-110">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="e61f6-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="e61f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="e61f6-111">PARAMETERS</span></span>

### <span data-ttu-id="e61f6-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e61f6-112">-Confirm</span></span>
<span data-ttu-id="e61f6-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e61f6-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e61f6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e61f6-114">-Force</span></span>
<span data-ttu-id="e61f6-115">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e61f6-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e61f6-116">-Local</span><span class="sxs-lookup"><span data-stu-id="e61f6-116">-Location</span></span>
<span data-ttu-id="e61f6-117">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="e61f6-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e61f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e61f6-118">-Name</span></span>
<span data-ttu-id="e61f6-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e61f6-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e61f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e61f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="e61f6-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e61f6-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e61f6-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="e61f6-122">-Tag</span></span>
<span data-ttu-id="e61f6-123">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e61f6-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e61f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e61f6-124">-WhatIf</span></span>
<span data-ttu-id="e61f6-125">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e61f6-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e61f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e61f6-126">-DefaultProfile</span></span>
<span data-ttu-id="e61f6-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e61f6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e61f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e61f6-128">CommonParameters</span></span>
<span data-ttu-id="e61f6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e61f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e61f6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e61f6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e61f6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e61f6-131">INPUTS</span></span>

### <span data-ttu-id="e61f6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e61f6-132">System.String</span></span>
<span data-ttu-id="e61f6-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e61f6-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e61f6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e61f6-134">OUTPUTS</span></span>

### <span data-ttu-id="e61f6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e61f6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e61f6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e61f6-136">NOTES</span></span>
<span data-ttu-id="e61f6-137">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e61f6-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e61f6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e61f6-138">RELATED LINKS</span></span>

[<span data-ttu-id="e61f6-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e61f6-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="e61f6-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e61f6-140">Remove-AzureRmDataFactoryV2</span></span>]()
