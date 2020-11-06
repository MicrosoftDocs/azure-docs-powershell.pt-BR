---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610012"
---
# <span data-ttu-id="23c88-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="23c88-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="23c88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23c88-102">SYNOPSIS</span></span>
<span data-ttu-id="23c88-103">Remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="23c88-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23c88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23c88-104">SYNTAX</span></span>

### <span data-ttu-id="23c88-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="23c88-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="23c88-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="23c88-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="23c88-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23c88-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="23c88-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23c88-108">DESCRIPTION</span></span>
<span data-ttu-id="23c88-109">O cmdlet Remove-AzureRmDataFactoryV2 remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="23c88-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="23c88-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23c88-110">EXAMPLES</span></span>

### <span data-ttu-id="23c88-111">Exemplo 1: remover uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="23c88-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="23c88-112">Esse comando Remove a fábrica de dados chamada WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="23c88-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="23c88-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="23c88-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="23c88-114">OS</span><span class="sxs-lookup"><span data-stu-id="23c88-114">PARAMETERS</span></span>

### <span data-ttu-id="23c88-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23c88-115">-Confirm</span></span>
<span data-ttu-id="23c88-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c88-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23c88-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23c88-117">-InputObject</span></span>
<span data-ttu-id="23c88-118">Especifica o objeto datafactory a ser removido.</span><span class="sxs-lookup"><span data-stu-id="23c88-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23c88-119">-Force</span><span class="sxs-lookup"><span data-stu-id="23c88-119">-Force</span></span>
<span data-ttu-id="23c88-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="23c88-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="23c88-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="23c88-121">-Name</span></span>
<span data-ttu-id="23c88-122">Especifica o nome da fábrica de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="23c88-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c88-123">-ResourceGroupName</span></span>
<span data-ttu-id="23c88-124">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="23c88-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="23c88-125">Esse cmdlet Remove uma fábrica de dados do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="23c88-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c88-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23c88-126">-ResourceId</span></span>
<span data-ttu-id="23c88-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="23c88-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c88-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c88-128">-WhatIf</span></span>
<span data-ttu-id="23c88-129">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c88-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="23c88-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23c88-130">INPUTS</span></span>

### <span data-ttu-id="23c88-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="23c88-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="23c88-132">System. String</span><span class="sxs-lookup"><span data-stu-id="23c88-132">System.String</span></span>


## <span data-ttu-id="23c88-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23c88-133">OUTPUTS</span></span>

### <span data-ttu-id="23c88-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="23c88-134">System.Object</span></span>

## <span data-ttu-id="23c88-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23c88-135">NOTES</span></span>
<span data-ttu-id="23c88-136">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="23c88-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="23c88-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23c88-137">RELATED LINKS</span></span>
[<span data-ttu-id="23c88-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="23c88-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="23c88-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="23c88-139">Set-AzureRmDataFactoryV2</span></span>]()
