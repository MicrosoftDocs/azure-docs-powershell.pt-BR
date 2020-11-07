---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778219"
---
# <span data-ttu-id="23531-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="23531-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="23531-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23531-102">SYNOPSIS</span></span>
<span data-ttu-id="23531-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="23531-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="23531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23531-104">SYNTAX</span></span>

### <span data-ttu-id="23531-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="23531-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23531-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="23531-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23531-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="23531-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23531-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="23531-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23531-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23531-109">DESCRIPTION</span></span>
<span data-ttu-id="23531-110">O cmdlet **Edit-AzRecoveryServicesAsrRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="23531-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="23531-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23531-111">EXAMPLES</span></span>

### <span data-ttu-id="23531-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23531-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="23531-113">Acrescenta um grupo ao plano existente do Azure site Recovery e retorna o plano de recuperação atualizado na memória.</span><span class="sxs-lookup"><span data-stu-id="23531-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="23531-114">OS</span><span class="sxs-lookup"><span data-stu-id="23531-114">PARAMETERS</span></span>

### <span data-ttu-id="23531-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="23531-115">-AddProtectedItem</span></span>
<span data-ttu-id="23531-116">Lista de itens protegidos de replicação ASR a serem adicionados ao grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="23531-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23531-117">-Append</span><span class="sxs-lookup"><span data-stu-id="23531-117">-AppendGroup</span></span>
<span data-ttu-id="23531-118">Parâmetro switch para acrescentar um grupo de plano de recuperação ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="23531-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23531-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23531-119">-DefaultProfile</span></span>
<span data-ttu-id="23531-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23531-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="23531-121">-Grupo</span><span class="sxs-lookup"><span data-stu-id="23531-121">-Group</span></span>
<span data-ttu-id="23531-122">Especifica um grupo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="23531-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23531-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23531-123">-InputObject</span></span>
<span data-ttu-id="23531-124">O objeto de plano de recuperação ASR a ser editado (na operação de memória.</span><span class="sxs-lookup"><span data-stu-id="23531-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="23531-125">Para atualizar o plano de recuperação execute Update-AzASRRecoveryPlan com o objeto do plano de recuperação editado.)</span><span class="sxs-lookup"><span data-stu-id="23531-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23531-126">-Remover o</span><span class="sxs-lookup"><span data-stu-id="23531-126">-RemoveGroup</span></span>
<span data-ttu-id="23531-127">Remove o grupo especificado do objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="23531-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23531-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="23531-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="23531-129">Lista de itens protegidos de replicação ASR a serem removidos do grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="23531-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23531-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23531-130">-Confirm</span></span>
<span data-ttu-id="23531-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23531-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23531-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23531-132">-WhatIf</span></span>
<span data-ttu-id="23531-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23531-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23531-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23531-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23531-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23531-135">CommonParameters</span></span>
<span data-ttu-id="23531-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23531-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23531-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23531-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23531-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23531-138">INPUTS</span></span>

### <span data-ttu-id="23531-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="23531-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="23531-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23531-140">OUTPUTS</span></span>

### <span data-ttu-id="23531-141">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="23531-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="23531-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23531-142">NOTES</span></span>

## <span data-ttu-id="23531-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23531-143">RELATED LINKS</span></span>

[<span data-ttu-id="23531-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="23531-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="23531-145">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="23531-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
