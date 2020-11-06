---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441576"
---
# <span data-ttu-id="f55fc-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f55fc-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f55fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f55fc-103">Remove um serviço vinculado da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f55fc-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f55fc-104">SYNTAX</span></span>

### <span data-ttu-id="f55fc-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f55fc-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f55fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f55fc-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f55fc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f55fc-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f55fc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f55fc-108">DESCRIPTION</span></span>
<span data-ttu-id="f55fc-109">O cmdlet Remove-AzureRmDataFactoryV2LinkedService remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f55fc-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f55fc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f55fc-110">EXAMPLES</span></span>

### <span data-ttu-id="f55fc-111">Exemplo 1: remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="f55fc-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="f55fc-112">Esse comando Remove o serviço vinculado denominado LinkedServiceTest do data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f55fc-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="f55fc-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="f55fc-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="f55fc-114">OS</span><span class="sxs-lookup"><span data-stu-id="f55fc-114">PARAMETERS</span></span>

### <span data-ttu-id="f55fc-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f55fc-115">-Confirm</span></span>
<span data-ttu-id="f55fc-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55fc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55fc-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f55fc-117">-DataFactoryName</span></span>
<span data-ttu-id="f55fc-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f55fc-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f55fc-119">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f55fc-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55fc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f55fc-120">-Force</span></span>
<span data-ttu-id="f55fc-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f55fc-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f55fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55fc-122">-InputObject</span></span>
<span data-ttu-id="f55fc-123">Especifica o objeto LinkedService a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f55fc-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55fc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f55fc-124">-Name</span></span>
<span data-ttu-id="f55fc-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f55fc-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="f55fc-126">Nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="f55fc-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="f55fc-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f55fc-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f55fc-129">Esse cmdlet Remove um serviço vinculado do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f55fc-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f55fc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f55fc-130">-ResourceId</span></span>
<span data-ttu-id="f55fc-131">A ID de recurso do Azure do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f55fc-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="f55fc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55fc-132">-WhatIf</span></span>
<span data-ttu-id="f55fc-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55fc-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="f55fc-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f55fc-134">INPUTS</span></span>

### <span data-ttu-id="f55fc-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f55fc-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="f55fc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f55fc-136">System.String</span></span>


## <span data-ttu-id="f55fc-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f55fc-137">OUTPUTS</span></span>

### <span data-ttu-id="f55fc-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="f55fc-138">System.Object</span></span>

## <span data-ttu-id="f55fc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f55fc-139">NOTES</span></span>
<span data-ttu-id="f55fc-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="f55fc-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f55fc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55fc-141">RELATED LINKS</span></span>
[<span data-ttu-id="f55fc-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f55fc-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f55fc-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f55fc-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

