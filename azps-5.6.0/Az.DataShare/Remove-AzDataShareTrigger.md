---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887202"
---
# <span data-ttu-id="fc99d-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="fc99d-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="fc99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc99d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc99d-103">remove um gatilho</span><span class="sxs-lookup"><span data-stu-id="fc99d-103">removes a trigger</span></span>

## <span data-ttu-id="fc99d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fc99d-104">SYNTAX</span></span>

### <span data-ttu-id="fc99d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fc99d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc99d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc99d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc99d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc99d-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc99d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fc99d-108">DESCRIPTION</span></span>
<span data-ttu-id="fc99d-109">O cmdlet **Remove-AzDataShareTrigger** remove um gatilho datashare</span><span class="sxs-lookup"><span data-stu-id="fc99d-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="fc99d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc99d-110">EXAMPLES</span></span>

### <span data-ttu-id="fc99d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc99d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="fc99d-112">Esses comandos removem um gatilho chamado AdsTrigger da assinatura de compartilhamento AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="fc99d-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="fc99d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fc99d-113">PARAMETERS</span></span>

### <span data-ttu-id="fc99d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc99d-114">-AccountName</span></span>
<span data-ttu-id="fc99d-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-115">Azure data share account name</span></span>

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

### <span data-ttu-id="fc99d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc99d-116">-AsJob</span></span>
<span data-ttu-id="fc99d-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="fc99d-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="fc99d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc99d-118">-DefaultProfile</span></span>
<span data-ttu-id="fc99d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc99d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc99d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc99d-120">-InputObject</span></span>
<span data-ttu-id="fc99d-121">Objeto disparador de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc99d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fc99d-122">-Name</span></span>
<span data-ttu-id="fc99d-123">Nome do gatilho de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="fc99d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc99d-124">-PassThru</span></span>
<span data-ttu-id="fc99d-125">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="fc99d-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="fc99d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc99d-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc99d-127">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fc99d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc99d-128">-ResourceId</span></span>
<span data-ttu-id="fc99d-129">A id de recurso do gatilho de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="fc99d-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fc99d-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="fc99d-131">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="fc99d-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc99d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc99d-132">-Confirm</span></span>
<span data-ttu-id="fc99d-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc99d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc99d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc99d-134">-WhatIf</span></span>
<span data-ttu-id="fc99d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc99d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc99d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc99d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc99d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc99d-137">CommonParameters</span></span>
<span data-ttu-id="fc99d-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc99d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc99d-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc99d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc99d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc99d-140">INPUTS</span></span>

### <span data-ttu-id="fc99d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fc99d-141">System.String</span></span>

### <span data-ttu-id="fc99d-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="fc99d-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="fc99d-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fc99d-143">OUTPUTS</span></span>

### <span data-ttu-id="fc99d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc99d-144">System.Boolean</span></span>

## <span data-ttu-id="fc99d-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="fc99d-145">NOTES</span></span>

## <span data-ttu-id="fc99d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc99d-146">RELATED LINKS</span></span>
