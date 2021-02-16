---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113279"
---
# <span data-ttu-id="f457f-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f457f-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f457f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f457f-102">SYNOPSIS</span></span>
<span data-ttu-id="f457f-103">Remove um pipeline do Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f457f-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="f457f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f457f-104">SYNTAX</span></span>

### <span data-ttu-id="f457f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f457f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f457f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f457f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f457f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f457f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f457f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f457f-108">DESCRIPTION</span></span>
<span data-ttu-id="f457f-109">O cmdlet Remove-AzDataFactoryV2Pipeline remove um pipeline do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f457f-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f457f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f457f-110">EXAMPLES</span></span>

### <span data-ttu-id="f457f-111">Exemplo 1: Remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="f457f-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="f457f-112">Este cmdlet remove o pipeline chamado DPWikisample da fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f457f-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="f457f-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="f457f-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="f457f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f457f-114">PARAMETERS</span></span>

### <span data-ttu-id="f457f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f457f-115">-DataFactoryName</span></span>
<span data-ttu-id="f457f-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f457f-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f457f-117">Este cmdlet remove um pipeline da fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f457f-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f457f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f457f-118">-DefaultProfile</span></span>
<span data-ttu-id="f457f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f457f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f457f-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f457f-120">-Force</span></span>
<span data-ttu-id="f457f-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f457f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f457f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f457f-122">-InputObject</span></span>
<span data-ttu-id="f457f-123">Especifica um objeto Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f457f-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="f457f-124">Este cmdlet remove o pipeline especificado por este parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f457f-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="f457f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f457f-125">-Name</span></span>
<span data-ttu-id="f457f-126">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f457f-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="f457f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f457f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f457f-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f457f-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f457f-129">Este cmdlet remove um pipeline do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f457f-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f457f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f457f-130">-ResourceId</span></span>
<span data-ttu-id="f457f-131">A ID de recurso do Azure do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f457f-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="f457f-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f457f-132">-Confirm</span></span>
<span data-ttu-id="f457f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f457f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f457f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f457f-134">-WhatIf</span></span>
<span data-ttu-id="f457f-135">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f457f-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f457f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f457f-136">CommonParameters</span></span>
<span data-ttu-id="f457f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f457f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f457f-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f457f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f457f-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="f457f-139">INPUTS</span></span>

### <span data-ttu-id="f457f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSInaline</span><span class="sxs-lookup"><span data-stu-id="f457f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="f457f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f457f-141">System.String</span></span>

## <span data-ttu-id="f457f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="f457f-142">OUTPUTS</span></span>

### <span data-ttu-id="f457f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f457f-143">System.Boolean</span></span>

## <span data-ttu-id="f457f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="f457f-144">NOTES</span></span>
<span data-ttu-id="f457f-145">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="f457f-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f457f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f457f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f457f-147">Get-AzDataFactoryV2Dataline</span><span class="sxs-lookup"><span data-stu-id="f457f-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f457f-148">Set-AzDataFactoryV2Dataline</span><span class="sxs-lookup"><span data-stu-id="f457f-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f457f-149">Invoke-AzDataFactoryV2 Invokeline</span><span class="sxs-lookup"><span data-stu-id="f457f-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

