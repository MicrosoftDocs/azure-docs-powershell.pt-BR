---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440192"
---
# <span data-ttu-id="a8cf7-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8cf7-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a8cf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cf7-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8cf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8cf7-104">SYNTAX</span></span>

### <span data-ttu-id="a8cf7-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="a8cf7-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8cf7-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="a8cf7-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cf7-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="a8cf7-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cf7-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="a8cf7-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8cf7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a8cf7-109">DESCRIPTION</span></span>
<span data-ttu-id="a8cf7-110">O cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="a8cf7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8cf7-111">EXAMPLES</span></span>

### <span data-ttu-id="a8cf7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8cf7-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="a8cf7-113">Acrescenta um grupo ao plano de recuperação do Azure site Recovery existente e retorna o plano de recuperação atualizado na memória.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="a8cf7-114">OS</span><span class="sxs-lookup"><span data-stu-id="a8cf7-114">PARAMETERS</span></span>

### <span data-ttu-id="a8cf7-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8cf7-115">-AddProtectedItem</span></span>
<span data-ttu-id="a8cf7-116">Lista de itens protegidos de replicação ASR a serem adicionados ao grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-117">-Append</span><span class="sxs-lookup"><span data-stu-id="a8cf7-117">-AppendGroup</span></span>
<span data-ttu-id="a8cf7-118">Parâmetro switch para acrescentar um grupo de plano de recuperação ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-119">-Grupo</span><span class="sxs-lookup"><span data-stu-id="a8cf7-119">-Group</span></span>
<span data-ttu-id="a8cf7-120">Especifica um grupo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8cf7-121">-InputObject</span></span>
<span data-ttu-id="a8cf7-122">O objeto de plano de recuperação ASR a ser editado (na operação de memória.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="a8cf7-123">Para atualizar o plano de recuperação execute Update-AzureRmASRRecoveryPlan com o objeto do plano de recuperação editado.)</span><span class="sxs-lookup"><span data-stu-id="a8cf7-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-124">-Remover o</span><span class="sxs-lookup"><span data-stu-id="a8cf7-124">-RemoveGroup</span></span>
<span data-ttu-id="a8cf7-125">Remove o grupo especificado do objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8cf7-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="a8cf7-127">Lista de itens protegidos de replicação ASR a serem removidos do grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a8cf7-128">-Confirm</span></span>
<span data-ttu-id="a8cf7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8cf7-130">-WhatIf</span></span>
<span data-ttu-id="a8cf7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8cf7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cf7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cf7-133">CommonParameters</span></span>
<span data-ttu-id="a8cf7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8cf7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cf7-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8cf7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cf7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a8cf7-136">INPUTS</span></span>

### <span data-ttu-id="a8cf7-137">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8cf7-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a8cf7-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a8cf7-138">OUTPUTS</span></span>

### <span data-ttu-id="a8cf7-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8cf7-139">System.Object</span></span>

## <span data-ttu-id="a8cf7-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a8cf7-140">NOTES</span></span>

## <span data-ttu-id="a8cf7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8cf7-141">RELATED LINKS</span></span>

[<span data-ttu-id="a8cf7-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8cf7-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a8cf7-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8cf7-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
