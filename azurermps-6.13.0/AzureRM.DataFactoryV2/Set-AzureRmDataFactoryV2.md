---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430330"
---
# <span data-ttu-id="68bd3-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68bd3-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="68bd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="68bd3-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68bd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68bd3-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68bd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68bd3-105">DESCRIPTION</span></span>
<span data-ttu-id="68bd3-106">O cmdlet **set-AzureRmDataFactoryV2** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="68bd3-107">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="68bd3-108">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-108">-- Create linked services.</span></span>
<span data-ttu-id="68bd3-109">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="68bd3-109">-- Create datasets.</span></span>
<span data-ttu-id="68bd3-110">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="68bd3-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="68bd3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68bd3-111">EXAMPLES</span></span>

### <span data-ttu-id="68bd3-112">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="68bd3-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="68bd3-113">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="68bd3-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="68bd3-114">OS</span><span class="sxs-lookup"><span data-stu-id="68bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="68bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="68bd3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68bd3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68bd3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="68bd3-117">-Force</span></span>
<span data-ttu-id="68bd3-118">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="68bd3-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="68bd3-119">-Local</span><span class="sxs-lookup"><span data-stu-id="68bd3-119">-Location</span></span>
<span data-ttu-id="68bd3-120">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="68bd3-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="68bd3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="68bd3-121">-Name</span></span>
<span data-ttu-id="68bd3-122">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-122">The data factory name.</span></span>

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

### <span data-ttu-id="68bd3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68bd3-123">-ResourceGroupName</span></span>
<span data-ttu-id="68bd3-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="68bd3-124">The resource group name.</span></span>

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

### <span data-ttu-id="68bd3-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="68bd3-125">-Tag</span></span>
<span data-ttu-id="68bd3-126">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="68bd3-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="68bd3-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68bd3-127">-Confirm</span></span>
<span data-ttu-id="68bd3-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68bd3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68bd3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68bd3-129">-WhatIf</span></span>
<span data-ttu-id="68bd3-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68bd3-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="68bd3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68bd3-131">CommonParameters</span></span>
<span data-ttu-id="68bd3-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68bd3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68bd3-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68bd3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68bd3-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68bd3-134">INPUTS</span></span>

### <span data-ttu-id="68bd3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="68bd3-135">System.String</span></span>

### <span data-ttu-id="68bd3-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="68bd3-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="68bd3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68bd3-137">OUTPUTS</span></span>

### <span data-ttu-id="68bd3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="68bd3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="68bd3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68bd3-139">NOTES</span></span>
<span data-ttu-id="68bd3-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="68bd3-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="68bd3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68bd3-141">RELATED LINKS</span></span>

[<span data-ttu-id="68bd3-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68bd3-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="68bd3-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="68bd3-143">Remove-AzureRmDataFactoryV2</span></span>]()
