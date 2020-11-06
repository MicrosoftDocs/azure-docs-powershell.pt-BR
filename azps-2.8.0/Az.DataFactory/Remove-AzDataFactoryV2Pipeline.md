---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 636ba1466eb0c5c0e8fda0433c74ec2291d2db9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596987"
---
# <span data-ttu-id="bf5e1-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="bf5e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5e1-103">Remove um pipeline da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="bf5e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf5e1-104">SYNTAX</span></span>

### <span data-ttu-id="bf5e1-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf5e1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf5e1-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5e1-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf5e1-108">DESCRIPTION</span></span>
<span data-ttu-id="bf5e1-109">O cmdlet Remove-AzDataFactoryV2Pipeline remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="bf5e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf5e1-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5e1-111">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="bf5e1-112">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="bf5e1-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="bf5e1-114">OS</span><span class="sxs-lookup"><span data-stu-id="bf5e1-114">PARAMETERS</span></span>

### <span data-ttu-id="bf5e1-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bf5e1-115">-DataFactoryName</span></span>
<span data-ttu-id="bf5e1-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bf5e1-117">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf5e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5e1-118">-DefaultProfile</span></span>
<span data-ttu-id="bf5e1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf5e1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bf5e1-120">-Force</span></span>
<span data-ttu-id="bf5e1-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="bf5e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5e1-122">-InputObject</span></span>
<span data-ttu-id="bf5e1-123">Especifica um objeto de pipeline.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="bf5e1-124">Esse cmdlet Remove o pipeline que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf5e1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf5e1-125">-Name</span></span>
<span data-ttu-id="bf5e1-126">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="bf5e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf5e1-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bf5e1-129">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf5e1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5e1-130">-ResourceId</span></span>
<span data-ttu-id="bf5e1-131">A ID de recurso do Azure do pipeline a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="bf5e1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf5e1-132">-Confirm</span></span>
<span data-ttu-id="bf5e1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf5e1-134">-WhatIf</span></span>
<span data-ttu-id="bf5e1-135">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="bf5e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5e1-136">CommonParameters</span></span>
<span data-ttu-id="bf5e1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5e1-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5e1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5e1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf5e1-139">INPUTS</span></span>

### <span data-ttu-id="bf5e1-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="bf5e1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf5e1-141">System.String</span></span>

## <span data-ttu-id="bf5e1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf5e1-142">OUTPUTS</span></span>

### <span data-ttu-id="bf5e1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf5e1-143">System.Boolean</span></span>

## <span data-ttu-id="bf5e1-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf5e1-144">NOTES</span></span>
<span data-ttu-id="bf5e1-145">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="bf5e1-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bf5e1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf5e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf5e1-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="bf5e1-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="bf5e1-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf5e1-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

