---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 8adaa00b08615bb687cbd481584875e9c91e7da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431035"
---
# <span data-ttu-id="e90c8-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e90c8-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="e90c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e90c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e90c8-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e90c8-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e90c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e90c8-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e90c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e90c8-105">DESCRIPTION</span></span>
<span data-ttu-id="e90c8-106">O cmdlet **New-AzureRmDataFactory** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="e90c8-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="e90c8-107">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="e90c8-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="e90c8-108">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e90c8-108">Create a data factory.</span></span> 
- <span data-ttu-id="e90c8-109">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="e90c8-109">Create linked services.</span></span> 
- <span data-ttu-id="e90c8-110">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="e90c8-110">Create datasets.</span></span> 
- <span data-ttu-id="e90c8-111">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="e90c8-111">Create a pipeline.</span></span>

## <span data-ttu-id="e90c8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e90c8-112">EXAMPLES</span></span>

### <span data-ttu-id="e90c8-113">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="e90c8-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="e90c8-114">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="e90c8-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="e90c8-115">OS</span><span class="sxs-lookup"><span data-stu-id="e90c8-115">PARAMETERS</span></span>

### <span data-ttu-id="e90c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90c8-116">-DefaultProfile</span></span>
<span data-ttu-id="e90c8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e90c8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90c8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e90c8-118">-Force</span></span>
<span data-ttu-id="e90c8-119">Indica que esse cmdlet substitui uma fábrica de dados existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e90c8-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e90c8-120">-Local</span><span class="sxs-lookup"><span data-stu-id="e90c8-120">-Location</span></span>
<span data-ttu-id="e90c8-121">Especifica o local para a fábrica de dados, como Westus ou Eastus.</span><span class="sxs-lookup"><span data-stu-id="e90c8-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="e90c8-122">Somente o Oesteus tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="e90c8-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="e90c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e90c8-123">-Name</span></span>
<span data-ttu-id="e90c8-124">Especifica o nome do alocador de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e90c8-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e90c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e90c8-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e90c8-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e90c8-127">Esse cmdlet cria uma fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e90c8-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e90c8-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="e90c8-128">-Tag</span></span>
<span data-ttu-id="e90c8-129">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e90c8-129">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e90c8-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e90c8-130">-Confirm</span></span>
<span data-ttu-id="e90c8-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e90c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e90c8-132">-WhatIf</span></span>
<span data-ttu-id="e90c8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e90c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e90c8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e90c8-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e90c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90c8-135">CommonParameters</span></span>
<span data-ttu-id="e90c8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90c8-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90c8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90c8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e90c8-138">INPUTS</span></span>

### <span data-ttu-id="e90c8-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e90c8-139">None</span></span>
<span data-ttu-id="e90c8-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e90c8-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e90c8-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e90c8-141">OUTPUTS</span></span>

### <span data-ttu-id="e90c8-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e90c8-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="e90c8-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e90c8-143">NOTES</span></span>
* <span data-ttu-id="e90c8-144">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e90c8-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e90c8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e90c8-145">RELATED LINKS</span></span>

[<span data-ttu-id="e90c8-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e90c8-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="e90c8-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="e90c8-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


