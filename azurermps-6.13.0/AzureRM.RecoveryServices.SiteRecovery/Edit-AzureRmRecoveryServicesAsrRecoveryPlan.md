---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431925"
---
# <span data-ttu-id="10ef6-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10ef6-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="10ef6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="10ef6-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="10ef6-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10ef6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10ef6-104">SYNTAX</span></span>

### <span data-ttu-id="10ef6-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="10ef6-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ef6-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="10ef6-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ef6-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="10ef6-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10ef6-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="10ef6-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10ef6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10ef6-109">DESCRIPTION</span></span>
<span data-ttu-id="10ef6-110">O cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10ef6-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="10ef6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10ef6-111">EXAMPLES</span></span>

### <span data-ttu-id="10ef6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10ef6-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="10ef6-113">Acrescenta um grupo ao plano de recuperação do Azure site Recovery existente e retorna o plano de recuperação atualizado na memória.</span><span class="sxs-lookup"><span data-stu-id="10ef6-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="10ef6-114">OS</span><span class="sxs-lookup"><span data-stu-id="10ef6-114">PARAMETERS</span></span>

### <span data-ttu-id="10ef6-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10ef6-115">-AddProtectedItem</span></span>
<span data-ttu-id="10ef6-116">Lista de itens protegidos de replicação ASR a serem adicionados ao grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10ef6-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="10ef6-117">-Append</span><span class="sxs-lookup"><span data-stu-id="10ef6-117">-AppendGroup</span></span>
<span data-ttu-id="10ef6-118">Parâmetro switch para acrescentar um grupo de plano de recuperação ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10ef6-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="10ef6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ef6-119">-DefaultProfile</span></span>
<span data-ttu-id="10ef6-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10ef6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ef6-121">-Grupo</span><span class="sxs-lookup"><span data-stu-id="10ef6-121">-Group</span></span>
<span data-ttu-id="10ef6-122">Especifica um grupo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10ef6-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="10ef6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10ef6-123">-InputObject</span></span>
<span data-ttu-id="10ef6-124">O objeto de plano de recuperação ASR a ser editado (na operação de memória.</span><span class="sxs-lookup"><span data-stu-id="10ef6-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="10ef6-125">Para atualizar o plano de recuperação execute Update-AzureRmASRRecoveryPlan com o objeto do plano de recuperação editado.)</span><span class="sxs-lookup"><span data-stu-id="10ef6-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="10ef6-126">-Remover o</span><span class="sxs-lookup"><span data-stu-id="10ef6-126">-RemoveGroup</span></span>
<span data-ttu-id="10ef6-127">Remove o grupo especificado do objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10ef6-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="10ef6-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="10ef6-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="10ef6-129">Lista de itens protegidos de replicação ASR a serem removidos do grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10ef6-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="10ef6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10ef6-130">-Confirm</span></span>
<span data-ttu-id="10ef6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ef6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10ef6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10ef6-132">-WhatIf</span></span>
<span data-ttu-id="10ef6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10ef6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10ef6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10ef6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10ef6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ef6-135">CommonParameters</span></span>
<span data-ttu-id="10ef6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ef6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ef6-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ef6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ef6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10ef6-138">INPUTS</span></span>

### <span data-ttu-id="10ef6-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10ef6-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="10ef6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10ef6-140">OUTPUTS</span></span>

### <span data-ttu-id="10ef6-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="10ef6-141">System.Object</span></span>

## <span data-ttu-id="10ef6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10ef6-142">NOTES</span></span>

## <span data-ttu-id="10ef6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10ef6-143">RELATED LINKS</span></span>

[<span data-ttu-id="10ef6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10ef6-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="10ef6-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="10ef6-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
