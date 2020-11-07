---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: dc80b30e02901aaa56185270cb775d7b9ea1f106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944422"
---
# <span data-ttu-id="b4d3b-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b4d3b-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="b4d3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d3b-103">Remove um gatilho</span><span class="sxs-lookup"><span data-stu-id="b4d3b-103">removes a trigger</span></span>

## <span data-ttu-id="b4d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d3b-104">SYNTAX</span></span>

### <span data-ttu-id="b4d3b-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4d3b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d3b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d3b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d3b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d3b-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d3b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d3b-109">O cmdlet **Remove-AzDataShareTrigger** remove um gatilho de compartilhamento de DataShare</span><span class="sxs-lookup"><span data-stu-id="b4d3b-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="b4d3b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="b4d3b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4d3b-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b4d3b-112">Esses comandos removem um gatilho chamado AdsTrigger da assinatura de compartilhamento AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="b4d3b-113">OS</span><span class="sxs-lookup"><span data-stu-id="b4d3b-113">PARAMETERS</span></span>

### <span data-ttu-id="b4d3b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4d3b-114">-AccountName</span></span>
<span data-ttu-id="b4d3b-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b4d3b-115">Azure data share account name</span></span>

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

### <span data-ttu-id="b4d3b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4d3b-116">-AsJob</span></span>
<span data-ttu-id="b4d3b-117">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="b4d3b-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b4d3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d3b-118">-DefaultProfile</span></span>
<span data-ttu-id="b4d3b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d3b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d3b-120">-InputObject</span></span>
<span data-ttu-id="b4d3b-121">Objeto de gatilho do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b4d3b-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="b4d3b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4d3b-122">-Name</span></span>
<span data-ttu-id="b4d3b-123">Nome do gatilho do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b4d3b-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b4d3b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4d3b-124">-PassThru</span></span>
<span data-ttu-id="b4d3b-125">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="b4d3b-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="b4d3b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d3b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4d3b-127">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b4d3b-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b4d3b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d3b-128">-ResourceId</span></span>
<span data-ttu-id="b4d3b-129">A ID do recurso do gatilho do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b4d3b-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="b4d3b-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b4d3b-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="b4d3b-131">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b4d3b-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b4d3b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4d3b-132">-Confirm</span></span>
<span data-ttu-id="b4d3b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d3b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d3b-134">-WhatIf</span></span>
<span data-ttu-id="b4d3b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4d3b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d3b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d3b-137">CommonParameters</span></span>
<span data-ttu-id="b4d3b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d3b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d3b-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d3b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d3b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4d3b-140">INPUTS</span></span>

### <span data-ttu-id="b4d3b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4d3b-141">System.String</span></span>

### <span data-ttu-id="b4d3b-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b4d3b-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="b4d3b-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4d3b-143">OUTPUTS</span></span>

### <span data-ttu-id="b4d3b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4d3b-144">System.Boolean</span></span>

## <span data-ttu-id="b4d3b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4d3b-145">NOTES</span></span>

## <span data-ttu-id="b4d3b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4d3b-146">RELATED LINKS</span></span>
