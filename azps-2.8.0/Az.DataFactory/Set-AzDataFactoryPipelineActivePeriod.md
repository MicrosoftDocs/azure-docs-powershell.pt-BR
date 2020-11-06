---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596980"
---
# <span data-ttu-id="21ff3-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="21ff3-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="21ff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="21ff3-103">Configura o período ativo para fatias de dados.</span><span class="sxs-lookup"><span data-stu-id="21ff3-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="21ff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21ff3-104">SYNTAX</span></span>

### <span data-ttu-id="21ff3-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="21ff3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ff3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="21ff3-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ff3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21ff3-107">DESCRIPTION</span></span>
<span data-ttu-id="21ff3-108">O cmdlet **set-AzDataFactoryPipelineActivePeriod** configura o período ativo para as fatias de dados que são processadas por um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="21ff3-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="21ff3-109">Se você usar o cmdlet Set-AzDataFactorySliceStatus para modificar o status de fatias de um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de pontos.</span><span class="sxs-lookup"><span data-stu-id="21ff3-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="21ff3-110">Depois de criar um pipeline, você pode especificar o período no qual ocorre o processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="21ff3-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="21ff3-111">Especificar o período ativo para um pipeline define a duração do tempo em que as fatias de dados são processadas com base nas propriedades de **disponibilidade** que foram definidas para cada conjunto de dados de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="21ff3-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="21ff3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21ff3-112">EXAMPLES</span></span>

### <span data-ttu-id="21ff3-113">Exemplo 1: configurar o período ativo</span><span class="sxs-lookup"><span data-stu-id="21ff3-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="21ff3-114">Esse comando configura o período ativo para as fatias de dados que o pipeline nomeadou DPWikisample processos.</span><span class="sxs-lookup"><span data-stu-id="21ff3-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="21ff3-115">O comando fornece pontos iniciais e finais para as fatias de dados como valores.</span><span class="sxs-lookup"><span data-stu-id="21ff3-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="21ff3-116">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="21ff3-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="21ff3-117">OS</span><span class="sxs-lookup"><span data-stu-id="21ff3-117">PARAMETERS</span></span>

### <span data-ttu-id="21ff3-118">-Resolver automaticamente</span><span class="sxs-lookup"><span data-stu-id="21ff3-118">-AutoResolve</span></span>
<span data-ttu-id="21ff3-119">Indica que esse cmdlet usa resolução automática.</span><span class="sxs-lookup"><span data-stu-id="21ff3-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="21ff3-120">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="21ff3-120">-DataFactory</span></span>
<span data-ttu-id="21ff3-121">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="21ff3-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="21ff3-122">Esse cmdlet modifica o período ativo para um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21ff3-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="21ff3-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="21ff3-123">-DataFactoryName</span></span>
<span data-ttu-id="21ff3-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="21ff3-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="21ff3-125">Esse cmdlet modifica o período ativo para um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21ff3-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="21ff3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ff3-126">-DefaultProfile</span></span>
<span data-ttu-id="21ff3-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21ff3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ff3-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="21ff3-128">-EndDateTime</span></span>
<span data-ttu-id="21ff3-129">Especifica o fim de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="21ff3-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="21ff3-130">O processamento de dados ocorre ou as fatias de dados são processadas dentro desse período.</span><span class="sxs-lookup"><span data-stu-id="21ff3-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="21ff3-131">Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="21ff3-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="21ff3-132">*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico) o designador de fuso horário padrão é UTC.</span><span class="sxs-lookup"><span data-stu-id="21ff3-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ff3-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="21ff3-133">-ForceRecalculate</span></span>
<span data-ttu-id="21ff3-134">Indica que esse cmdlet usa recálculo forçado.</span><span class="sxs-lookup"><span data-stu-id="21ff3-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="21ff3-135">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="21ff3-135">-PipelineName</span></span>
<span data-ttu-id="21ff3-136">Especifica o nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="21ff3-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="21ff3-137">Esse cmdlet define o período ativo para o pipeline especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="21ff3-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ff3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ff3-138">-ResourceGroupName</span></span>
<span data-ttu-id="21ff3-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="21ff3-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="21ff3-140">Esse cmdlet modifica o período ativo para um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21ff3-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="21ff3-141">-StartDatetime</span><span class="sxs-lookup"><span data-stu-id="21ff3-141">-StartDateTime</span></span>
<span data-ttu-id="21ff3-142">Especifica o início de um período de tempo como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="21ff3-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="21ff3-143">O processamento de dados ocorre ou as fatias de dados são processadas dentro desse período.</span><span class="sxs-lookup"><span data-stu-id="21ff3-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="21ff3-144">*StartDateTime* deve ser especificado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="21ff3-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ff3-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21ff3-145">-Confirm</span></span>
<span data-ttu-id="21ff3-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21ff3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ff3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ff3-147">-WhatIf</span></span>
<span data-ttu-id="21ff3-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21ff3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ff3-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21ff3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ff3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ff3-150">CommonParameters</span></span>
<span data-ttu-id="21ff3-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ff3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ff3-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ff3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ff3-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21ff3-153">INPUTS</span></span>

### <span data-ttu-id="21ff3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="21ff3-154">System.String</span></span>

### <span data-ttu-id="21ff3-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="21ff3-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="21ff3-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21ff3-156">OUTPUTS</span></span>

### <span data-ttu-id="21ff3-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21ff3-157">System.Boolean</span></span>

## <span data-ttu-id="21ff3-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21ff3-158">NOTES</span></span>
* <span data-ttu-id="21ff3-159">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="21ff3-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="21ff3-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21ff3-160">RELATED LINKS</span></span>

[<span data-ttu-id="21ff3-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21ff3-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="21ff3-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="21ff3-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


