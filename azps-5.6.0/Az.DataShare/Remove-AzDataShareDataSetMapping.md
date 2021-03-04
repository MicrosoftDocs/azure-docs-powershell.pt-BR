---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889984"
---
# <span data-ttu-id="57afd-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="57afd-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="57afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57afd-102">SYNOPSIS</span></span>
<span data-ttu-id="57afd-103">Remove um mapeamento de conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="57afd-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="57afd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57afd-104">SYNTAX</span></span>

### <span data-ttu-id="57afd-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57afd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57afd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57afd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57afd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57afd-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57afd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57afd-108">DESCRIPTION</span></span>
<span data-ttu-id="57afd-109">O cmdlet **Remove-AzDataShareDataSetMapping** remove um mapeamentos de conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="57afd-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="57afd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57afd-110">EXAMPLES</span></span>

### <span data-ttu-id="57afd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57afd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="57afd-112">Esses comandos removem o conjuntos de dados chamado DSM do WikiAds de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="57afd-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="57afd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57afd-113">PARAMETERS</span></span>

### <span data-ttu-id="57afd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57afd-114">-AccountName</span></span>
<span data-ttu-id="57afd-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="57afd-115">Azure data share account name</span></span>

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

### <span data-ttu-id="57afd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57afd-116">-DefaultProfile</span></span>
<span data-ttu-id="57afd-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57afd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57afd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57afd-118">-InputObject</span></span>
<span data-ttu-id="57afd-119">O objeto de mapeamento do conjunto de dados do azure</span><span class="sxs-lookup"><span data-stu-id="57afd-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57afd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57afd-120">-Name</span></span>
<span data-ttu-id="57afd-121">Nome do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="57afd-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="57afd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57afd-122">-PassThru</span></span>
<span data-ttu-id="57afd-123">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="57afd-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="57afd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57afd-124">-ResourceGroupName</span></span>
<span data-ttu-id="57afd-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="57afd-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="57afd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57afd-126">-ResourceId</span></span>
<span data-ttu-id="57afd-127">A id de recurso do mapeamento do conjunto de dados do azure</span><span class="sxs-lookup"><span data-stu-id="57afd-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="57afd-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="57afd-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="57afd-129">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="57afd-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="57afd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57afd-130">-Confirm</span></span>
<span data-ttu-id="57afd-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57afd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57afd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57afd-132">-WhatIf</span></span>
<span data-ttu-id="57afd-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57afd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57afd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57afd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57afd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57afd-135">CommonParameters</span></span>
<span data-ttu-id="57afd-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57afd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57afd-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57afd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57afd-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57afd-138">INPUTS</span></span>

### <span data-ttu-id="57afd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57afd-139">System.String</span></span>

### <span data-ttu-id="57afd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="57afd-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="57afd-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57afd-141">OUTPUTS</span></span>

### <span data-ttu-id="57afd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57afd-142">System.Boolean</span></span>

## <span data-ttu-id="57afd-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="57afd-143">NOTES</span></span>

## <span data-ttu-id="57afd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57afd-144">RELATED LINKS</span></span>
