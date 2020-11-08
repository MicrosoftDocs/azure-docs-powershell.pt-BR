---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114562"
---
# <span data-ttu-id="e005d-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e005d-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e005d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e005d-102">SYNOPSIS</span></span>
<span data-ttu-id="e005d-103">Inicia a sincronização de uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e005d-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="e005d-104">Uma assinatura de compartilhamento pode ser especificada por meio da ID do recurso ou do seu nome.</span><span class="sxs-lookup"><span data-stu-id="e005d-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="e005d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e005d-105">SYNTAX</span></span>

### <span data-ttu-id="e005d-106">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e005d-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e005d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e005d-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e005d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e005d-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e005d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e005d-109">DESCRIPTION</span></span>
<span data-ttu-id="e005d-110">O cmdlet **Start-AzDataShareSubscriptionSynchronization** inicia a sincronização de uma assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e005d-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="e005d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e005d-111">EXAMPLES</span></span>

### <span data-ttu-id="e005d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e005d-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="e005d-113">Esses comandos iniciam a sincronização de um sharesubscription chamado AdsShareSubscription na conta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="e005d-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="e005d-114">OS</span><span class="sxs-lookup"><span data-stu-id="e005d-114">PARAMETERS</span></span>

### <span data-ttu-id="e005d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e005d-115">-AccountName</span></span>
<span data-ttu-id="e005d-116">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e005d-116">Azure data share account name</span></span>

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

### <span data-ttu-id="e005d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e005d-117">-AsJob</span></span>
<span data-ttu-id="e005d-118">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="e005d-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="e005d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e005d-119">-DefaultProfile</span></span>
<span data-ttu-id="e005d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e005d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e005d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e005d-121">-InputObject</span></span>
<span data-ttu-id="e005d-122">Objeto de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e005d-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="e005d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e005d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e005d-124">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="e005d-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e005d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e005d-125">-ResourceId</span></span>
<span data-ttu-id="e005d-126">A ID do recurso da assinatura do Azure share</span><span class="sxs-lookup"><span data-stu-id="e005d-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="e005d-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e005d-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="e005d-128">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e005d-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e005d-129">-Synchronizationmode</span><span class="sxs-lookup"><span data-stu-id="e005d-129">-SynchronizationMode</span></span>
<span data-ttu-id="e005d-130">Modo de sincronização (FullSync ou incremental)</span><span class="sxs-lookup"><span data-stu-id="e005d-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="e005d-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e005d-131">-Confirm</span></span>
<span data-ttu-id="e005d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e005d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e005d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e005d-133">-WhatIf</span></span>
<span data-ttu-id="e005d-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e005d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e005d-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e005d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e005d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e005d-136">CommonParameters</span></span>
<span data-ttu-id="e005d-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e005d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e005d-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e005d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e005d-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e005d-139">INPUTS</span></span>

### <span data-ttu-id="e005d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e005d-140">System.String</span></span>

### <span data-ttu-id="e005d-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e005d-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="e005d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e005d-142">OUTPUTS</span></span>

### <span data-ttu-id="e005d-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e005d-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e005d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e005d-144">NOTES</span></span>

## <span data-ttu-id="e005d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e005d-145">RELATED LINKS</span></span>
