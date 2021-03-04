---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892647"
---
# <span data-ttu-id="43709-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="43709-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="43709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43709-102">SYNOPSIS</span></span>
<span data-ttu-id="43709-103">remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="43709-103">removes a share subscription</span></span>

## <span data-ttu-id="43709-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="43709-104">SYNTAX</span></span>

### <span data-ttu-id="43709-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43709-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43709-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43709-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43709-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43709-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43709-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="43709-108">DESCRIPTION</span></span>
<span data-ttu-id="43709-109">O cmdlet **Remove-AzDataShareSubscription** remove uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="43709-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="43709-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43709-110">EXAMPLES</span></span>

### <span data-ttu-id="43709-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43709-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="43709-112">Esses comandos removem uma assinatura de compartilhamento chamada AdsShareSubscription da conta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="43709-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="43709-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="43709-113">PARAMETERS</span></span>

### <span data-ttu-id="43709-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43709-114">-AccountName</span></span>
<span data-ttu-id="43709-115">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="43709-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="43709-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43709-116">-AsJob</span></span>
<span data-ttu-id="43709-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="43709-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="43709-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43709-118">-DefaultProfile</span></span>
<span data-ttu-id="43709-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43709-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43709-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43709-120">-InputObject</span></span>
<span data-ttu-id="43709-121">Objeto de assinatura de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="43709-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43709-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43709-122">-Name</span></span>
<span data-ttu-id="43709-123">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="43709-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="43709-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43709-124">-PassThru</span></span>
<span data-ttu-id="43709-125">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="43709-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="43709-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43709-126">-ResourceGroupName</span></span>
<span data-ttu-id="43709-127">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="43709-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="43709-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43709-128">-ResourceId</span></span>
<span data-ttu-id="43709-129">A id de recurso da assinatura de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="43709-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="43709-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43709-130">-Confirm</span></span>
<span data-ttu-id="43709-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43709-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43709-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43709-132">-WhatIf</span></span>
<span data-ttu-id="43709-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43709-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43709-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43709-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43709-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43709-135">CommonParameters</span></span>
<span data-ttu-id="43709-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43709-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43709-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43709-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43709-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43709-138">INPUTS</span></span>

### <span data-ttu-id="43709-139">System.String</span><span class="sxs-lookup"><span data-stu-id="43709-139">System.String</span></span>

### <span data-ttu-id="43709-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="43709-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="43709-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="43709-141">OUTPUTS</span></span>

### <span data-ttu-id="43709-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43709-142">System.Boolean</span></span>

## <span data-ttu-id="43709-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="43709-143">NOTES</span></span>

## <span data-ttu-id="43709-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43709-144">RELATED LINKS</span></span>
