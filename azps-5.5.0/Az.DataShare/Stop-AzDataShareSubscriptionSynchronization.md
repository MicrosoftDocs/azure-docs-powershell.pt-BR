---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117713"
---
# <span data-ttu-id="28b4f-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="28b4f-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="28b4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="28b4f-103">Interrompe a sincronização contínua de uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="28b4f-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="28b4f-104">Uma assinatura de compartilhamento pode ser especificada por meio de sua ID de recurso ou seu nome.</span><span class="sxs-lookup"><span data-stu-id="28b4f-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="28b4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28b4f-105">SYNTAX</span></span>

### <span data-ttu-id="28b4f-106">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28b4f-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b4f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b4f-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b4f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b4f-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b4f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="28b4f-109">DESCRIPTION</span></span>
<span data-ttu-id="28b4f-110">O cmdlet **Stop-AzDataShareSubscriptionSynchronization** interrompe a sincronização contínua de uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="28b4f-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="28b4f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28b4f-111">EXAMPLES</span></span>

### <span data-ttu-id="28b4f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28b4f-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="28b4f-113">Interrompe a sincronização contínua identificada por id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="28b4f-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="28b4f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28b4f-114">PARAMETERS</span></span>

### <span data-ttu-id="28b4f-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="28b4f-115">-AccountName</span></span>
<span data-ttu-id="28b4f-116">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="28b4f-116">Azure data share account name</span></span>

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

### <span data-ttu-id="28b4f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28b4f-117">-AsJob</span></span>
<span data-ttu-id="28b4f-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="28b4f-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="28b4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b4f-119">-DefaultProfile</span></span>
<span data-ttu-id="28b4f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28b4f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b4f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28b4f-121">-InputObject</span></span>
<span data-ttu-id="28b4f-122">Objeto de assinatura de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="28b4f-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="28b4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="28b4f-124">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="28b4f-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="28b4f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b4f-125">-ResourceId</span></span>
<span data-ttu-id="28b4f-126">A ID do recurso da assinatura de compartilhamento do azure</span><span class="sxs-lookup"><span data-stu-id="28b4f-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="28b4f-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="28b4f-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="28b4f-128">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="28b4f-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="28b4f-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="28b4f-129">-SynchronizationId</span></span>
<span data-ttu-id="28b4f-130">ID de sincronização que precisa ser interrompida</span><span class="sxs-lookup"><span data-stu-id="28b4f-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b4f-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="28b4f-131">-Confirm</span></span>
<span data-ttu-id="28b4f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b4f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b4f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b4f-133">-WhatIf</span></span>
<span data-ttu-id="28b4f-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="28b4f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b4f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28b4f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b4f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b4f-136">CommonParameters</span></span>
<span data-ttu-id="28b4f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b4f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b4f-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28b4f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b4f-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="28b4f-139">INPUTS</span></span>

### <span data-ttu-id="28b4f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="28b4f-140">System.String</span></span>

### <span data-ttu-id="28b4f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="28b4f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="28b4f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="28b4f-142">OUTPUTS</span></span>

### <span data-ttu-id="28b4f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="28b4f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="28b4f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="28b4f-144">NOTES</span></span>

## <span data-ttu-id="28b4f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28b4f-145">RELATED LINKS</span></span>
