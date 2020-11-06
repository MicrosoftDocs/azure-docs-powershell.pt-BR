---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 48638f53f58fd420e9a7b3dfe2e50a3e61d2314f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427972"
---
# <span data-ttu-id="f5f83-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="f5f83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5f83-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f83-103">Remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5f83-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5f83-104">SYNTAX</span></span>

### <span data-ttu-id="f5f83-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5f83-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f83-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5f83-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f83-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5f83-107">DESCRIPTION</span></span>
<span data-ttu-id="f5f83-108">O cmdlet **Remove-AzureRmDataFactoryPipeline** remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5f83-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="f5f83-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5f83-109">EXAMPLES</span></span>

### <span data-ttu-id="f5f83-110">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="f5f83-111">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f5f83-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="f5f83-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="f5f83-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f5f83-113">OS</span><span class="sxs-lookup"><span data-stu-id="f5f83-113">PARAMETERS</span></span>

### <span data-ttu-id="f5f83-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="f5f83-114">-DataFactory</span></span>
<span data-ttu-id="f5f83-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f5f83-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f5f83-116">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f5f83-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f83-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f5f83-117">-DataFactoryName</span></span>
<span data-ttu-id="f5f83-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f5f83-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5f83-119">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f5f83-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f83-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f5f83-120">-Force</span></span>
<span data-ttu-id="f5f83-121">Indica que esse cmdlet Remove um pipeline sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5f83-121">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f5f83-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5f83-122">-Name</span></span>
<span data-ttu-id="f5f83-123">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f5f83-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="f5f83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f83-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5f83-125">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f83-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5f83-126">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f5f83-126">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f83-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5f83-127">-Confirm</span></span>
<span data-ttu-id="f5f83-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f83-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f83-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f83-129">-WhatIf</span></span>
<span data-ttu-id="f5f83-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5f83-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f83-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5f83-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f83-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f83-132">-DefaultProfile</span></span>
<span data-ttu-id="f5f83-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f83-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f83-134">CommonParameters</span></span>
<span data-ttu-id="f5f83-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f83-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f83-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f83-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5f83-137">INPUTS</span></span>

## <span data-ttu-id="f5f83-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5f83-138">OUTPUTS</span></span>

### <span data-ttu-id="f5f83-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5f83-139">System.Boolean</span></span>

## <span data-ttu-id="f5f83-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5f83-140">NOTES</span></span>
* <span data-ttu-id="f5f83-141">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="f5f83-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5f83-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5f83-142">RELATED LINKS</span></span>

[<span data-ttu-id="f5f83-143">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-143">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f5f83-144">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-144">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f5f83-145">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="f5f83-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f5f83-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f5f83-147">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f5f83-147">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


