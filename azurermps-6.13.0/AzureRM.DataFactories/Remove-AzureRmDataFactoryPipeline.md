---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: aede985cfac5b8ab25c4056eb44e54ea7c6b1c2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432021"
---
# <span data-ttu-id="7d680-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="7d680-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d680-102">SYNOPSIS</span></span>
<span data-ttu-id="7d680-103">Remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="7d680-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d680-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d680-104">SYNTAX</span></span>

### <span data-ttu-id="7d680-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d680-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d680-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7d680-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d680-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d680-107">DESCRIPTION</span></span>
<span data-ttu-id="7d680-108">O cmdlet **Remove-AzureRmDataFactoryPipeline** remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="7d680-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="7d680-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d680-109">EXAMPLES</span></span>

### <span data-ttu-id="7d680-110">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="7d680-111">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7d680-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="7d680-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="7d680-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="7d680-113">OS</span><span class="sxs-lookup"><span data-stu-id="7d680-113">PARAMETERS</span></span>

### <span data-ttu-id="7d680-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="7d680-114">-DataFactory</span></span>
<span data-ttu-id="7d680-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="7d680-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7d680-116">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7d680-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7d680-117">-DataFactoryName</span></span>
<span data-ttu-id="7d680-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7d680-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7d680-119">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7d680-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d680-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d680-120">-DefaultProfile</span></span>
<span data-ttu-id="7d680-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7d680-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d680-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7d680-122">-Force</span></span>
<span data-ttu-id="7d680-123">Indica que esse cmdlet Remove um pipeline sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="7d680-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7d680-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d680-124">-Name</span></span>
<span data-ttu-id="7d680-125">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7d680-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d680-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d680-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d680-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7d680-128">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7d680-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d680-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d680-129">-Confirm</span></span>
<span data-ttu-id="7d680-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d680-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d680-131">-WhatIf</span></span>
<span data-ttu-id="7d680-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d680-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d680-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d680-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d680-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d680-134">CommonParameters</span></span>
<span data-ttu-id="7d680-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d680-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d680-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d680-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d680-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d680-137">INPUTS</span></span>

### <span data-ttu-id="7d680-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7d680-138">System.String</span></span>

### <span data-ttu-id="7d680-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d680-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="7d680-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d680-140">OUTPUTS</span></span>

### <span data-ttu-id="7d680-141">System. void</span><span class="sxs-lookup"><span data-stu-id="7d680-141">System.Void</span></span>

## <span data-ttu-id="7d680-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d680-142">NOTES</span></span>
* <span data-ttu-id="7d680-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="7d680-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7d680-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d680-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d680-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="7d680-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="7d680-147">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="7d680-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="7d680-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="7d680-149">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d680-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


