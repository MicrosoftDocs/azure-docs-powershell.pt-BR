---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 8ede4fe94eccd9d9f08977a0af9cc8847e4aca1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892181"
---
# <span data-ttu-id="797ae-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="797ae-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="797ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797ae-102">SYNOPSIS</span></span>
<span data-ttu-id="797ae-103">Remove um mapeamento de conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="797ae-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="797ae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="797ae-104">SYNTAX</span></span>

### <span data-ttu-id="797ae-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="797ae-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="797ae-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797ae-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="797ae-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797ae-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="797ae-108">DESCRIPTION</span></span>
<span data-ttu-id="797ae-109">O cmdlet **Remove-AzDataShareDataSet** remove um conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="797ae-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="797ae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="797ae-110">EXAMPLES</span></span>

### <span data-ttu-id="797ae-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="797ae-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="797ae-112">Esses comandos removem o conjuntos de dados chamado DS do compartilhamento wikiAds.</span><span class="sxs-lookup"><span data-stu-id="797ae-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="797ae-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="797ae-113">PARAMETERS</span></span>

### <span data-ttu-id="797ae-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="797ae-114">-AccountName</span></span>
<span data-ttu-id="797ae-115">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797ae-116">-DefaultProfile</span></span>
<span data-ttu-id="797ae-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="797ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="797ae-118">-InputObject</span></span>
<span data-ttu-id="797ae-119">O objeto conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="797ae-120">-Name</span></span>
<span data-ttu-id="797ae-121">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="797ae-122">-PassThru</span></span>
<span data-ttu-id="797ae-123">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="797ae-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="797ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="797ae-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-125">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="797ae-126">-ResourceId</span></span>
<span data-ttu-id="797ae-127">A id de recurso do conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-127">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="797ae-128">-ShareName</span></span>
<span data-ttu-id="797ae-129">Nome do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="797ae-129">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797ae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="797ae-130">-Confirm</span></span>
<span data-ttu-id="797ae-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="797ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797ae-132">-WhatIf</span></span>
<span data-ttu-id="797ae-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="797ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="797ae-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="797ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="797ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797ae-135">CommonParameters</span></span>
<span data-ttu-id="797ae-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="797ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797ae-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="797ae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797ae-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="797ae-138">INPUTS</span></span>

### <span data-ttu-id="797ae-139">System.String</span><span class="sxs-lookup"><span data-stu-id="797ae-139">System.String</span></span>

### <span data-ttu-id="797ae-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="797ae-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="797ae-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="797ae-141">OUTPUTS</span></span>

### <span data-ttu-id="797ae-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="797ae-142">System.Boolean</span></span>

## <span data-ttu-id="797ae-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="797ae-143">NOTES</span></span>

## <span data-ttu-id="797ae-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="797ae-144">RELATED LINKS</span></span>
