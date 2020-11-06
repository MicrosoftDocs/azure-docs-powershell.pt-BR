---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: ed3284445121bf2ab6ecdd9aef2d8abe6d1351f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426381"
---
# <span data-ttu-id="b0631-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b0631-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0631-102">SYNOPSIS</span></span>
<span data-ttu-id="b0631-103">Remove um pipeline da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0631-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0631-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0631-104">SYNTAX</span></span>

### <span data-ttu-id="b0631-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0631-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0631-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b0631-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0631-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0631-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0631-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0631-108">DESCRIPTION</span></span>
<span data-ttu-id="b0631-109">O cmdlet Remove-AzureRmDataFactoryV2Pipeline remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="b0631-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="b0631-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0631-110">EXAMPLES</span></span>

### <span data-ttu-id="b0631-111">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b0631-112">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b0631-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="b0631-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="b0631-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="b0631-114">OS</span><span class="sxs-lookup"><span data-stu-id="b0631-114">PARAMETERS</span></span>

### <span data-ttu-id="b0631-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b0631-115">-DataFactoryName</span></span>
<span data-ttu-id="b0631-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0631-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b0631-117">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b0631-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0631-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0631-118">-DefaultProfile</span></span>
<span data-ttu-id="b0631-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0631-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0631-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b0631-120">-Force</span></span>
<span data-ttu-id="b0631-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b0631-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b0631-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0631-122">-InputObject</span></span>
<span data-ttu-id="b0631-123">Especifica um objeto de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0631-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="b0631-124">Esse cmdlet Remove o pipeline que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b0631-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0631-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0631-125">-Name</span></span>
<span data-ttu-id="b0631-126">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b0631-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0631-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0631-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0631-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0631-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b0631-129">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b0631-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0631-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0631-130">-ResourceId</span></span>
<span data-ttu-id="b0631-131">A ID de recurso do Azure do pipeline a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b0631-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0631-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0631-132">-Confirm</span></span>
<span data-ttu-id="b0631-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0631-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0631-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0631-134">-WhatIf</span></span>
<span data-ttu-id="b0631-135">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0631-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b0631-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0631-136">CommonParameters</span></span>
<span data-ttu-id="b0631-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0631-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0631-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0631-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0631-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0631-139">INPUTS</span></span>

### <span data-ttu-id="b0631-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="b0631-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0631-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b0631-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0631-142">System.String</span></span>

## <span data-ttu-id="b0631-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0631-143">OUTPUTS</span></span>

### <span data-ttu-id="b0631-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0631-144">System.Boolean</span></span>

## <span data-ttu-id="b0631-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0631-145">NOTES</span></span>
<span data-ttu-id="b0631-146">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="b0631-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b0631-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0631-147">RELATED LINKS</span></span>

[<span data-ttu-id="b0631-148">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-148">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b0631-149">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-149">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b0631-150">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b0631-150">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

