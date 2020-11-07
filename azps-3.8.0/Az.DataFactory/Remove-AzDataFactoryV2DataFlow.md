---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940470"
---
# <span data-ttu-id="c98f1-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="c98f1-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="c98f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c98f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c98f1-103">Remove um fluxo de dados da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c98f1-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="c98f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c98f1-104">SYNTAX</span></span>

### <span data-ttu-id="c98f1-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c98f1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c98f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c98f1-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98f1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c98f1-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98f1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c98f1-108">DESCRIPTION</span></span>
<span data-ttu-id="c98f1-109">O cmdlet Remove-AzDataFactoryV2DataFlow remove um fluxo de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c98f1-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="c98f1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c98f1-110">EXAMPLES</span></span>

### <span data-ttu-id="c98f1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c98f1-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="c98f1-112">Esse comando Remove o fluxo de dados chamado dataflow5 da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c98f1-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="c98f1-113">OS</span><span class="sxs-lookup"><span data-stu-id="c98f1-113">PARAMETERS</span></span>

### <span data-ttu-id="c98f1-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c98f1-114">-DataFactoryName</span></span>
<span data-ttu-id="c98f1-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="c98f1-115">The data factory name.</span></span>

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

### <span data-ttu-id="c98f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98f1-116">-DefaultProfile</span></span>
<span data-ttu-id="c98f1-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c98f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98f1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c98f1-118">-Force</span></span>
<span data-ttu-id="c98f1-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c98f1-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c98f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c98f1-120">-InputObject</span></span>
<span data-ttu-id="c98f1-121">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c98f1-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98f1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c98f1-122">-Name</span></span>
<span data-ttu-id="c98f1-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c98f1-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="c98f1-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c98f1-125">The resource group name.</span></span>

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

### <span data-ttu-id="c98f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c98f1-126">-ResourceId</span></span>
<span data-ttu-id="c98f1-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="c98f1-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c98f1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c98f1-128">-PassThru</span></span>
<span data-ttu-id="c98f1-129">Se especificado, a operação será gravada true se a operação do caso for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c98f1-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c98f1-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c98f1-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="c98f1-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c98f1-131">-Confirm</span></span>
<span data-ttu-id="c98f1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c98f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98f1-133">-WhatIf</span></span>
<span data-ttu-id="c98f1-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c98f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98f1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c98f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c98f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98f1-136">CommonParameters</span></span>
<span data-ttu-id="c98f1-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98f1-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c98f1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98f1-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c98f1-139">INPUTS</span></span>

### <span data-ttu-id="c98f1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c98f1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="c98f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c98f1-141">System.String</span></span>

## <span data-ttu-id="c98f1-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c98f1-142">OUTPUTS</span></span>

### <span data-ttu-id="c98f1-143">System. void</span><span class="sxs-lookup"><span data-stu-id="c98f1-143">System.Void</span></span>

### <span data-ttu-id="c98f1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c98f1-144">System.Boolean</span></span>

## <span data-ttu-id="c98f1-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c98f1-145">NOTES</span></span>
<span data-ttu-id="c98f1-146">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c98f1-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c98f1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c98f1-147">RELATED LINKS</span></span>

[<span data-ttu-id="c98f1-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c98f1-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="c98f1-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c98f1-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

