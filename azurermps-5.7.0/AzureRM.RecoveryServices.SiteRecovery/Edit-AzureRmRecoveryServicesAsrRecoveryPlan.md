---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 289804771010a586b73621ec5df81805ed30ae55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432428"
---
# <span data-ttu-id="da91f-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da91f-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="da91f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da91f-102">SYNOPSIS</span></span>
<span data-ttu-id="da91f-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="da91f-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da91f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da91f-104">SYNTAX</span></span>

### <span data-ttu-id="da91f-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="da91f-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da91f-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="da91f-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da91f-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="da91f-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da91f-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="da91f-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da91f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da91f-109">DESCRIPTION</span></span>
<span data-ttu-id="da91f-110">O cmdlet **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="da91f-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="da91f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da91f-111">EXAMPLES</span></span>

### <span data-ttu-id="da91f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da91f-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="da91f-113">Acrescenta um grupo ao plano de recuperação do Azure site Recovery existente e retorna o plano de recuperação atualizado na memória.</span><span class="sxs-lookup"><span data-stu-id="da91f-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="da91f-114">OS</span><span class="sxs-lookup"><span data-stu-id="da91f-114">PARAMETERS</span></span>

### <span data-ttu-id="da91f-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da91f-115">-AddProtectedItem</span></span>
<span data-ttu-id="da91f-116">Lista de itens protegidos de replicação ASR a serem adicionados ao grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da91f-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="da91f-117">-Append</span><span class="sxs-lookup"><span data-stu-id="da91f-117">-AppendGroup</span></span>
<span data-ttu-id="da91f-118">Parâmetro switch para acrescentar um grupo de plano de recuperação ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da91f-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="da91f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da91f-119">-Confirm</span></span>
<span data-ttu-id="da91f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da91f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da91f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da91f-121">-DefaultProfile</span></span>
<span data-ttu-id="da91f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da91f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da91f-123">-Grupo</span><span class="sxs-lookup"><span data-stu-id="da91f-123">-Group</span></span>
<span data-ttu-id="da91f-124">Especifica um grupo de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da91f-124">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="da91f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da91f-125">-InputObject</span></span>
<span data-ttu-id="da91f-126">O objeto de plano de recuperação ASR a ser editado (na operação de memória.</span><span class="sxs-lookup"><span data-stu-id="da91f-126">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="da91f-127">Para atualizar o plano de recuperação execute Update-AzureRmASRRecoveryPlan com o objeto do plano de recuperação editado.)</span><span class="sxs-lookup"><span data-stu-id="da91f-127">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="da91f-128">-Remover o</span><span class="sxs-lookup"><span data-stu-id="da91f-128">-RemoveGroup</span></span>
<span data-ttu-id="da91f-129">Remove o grupo especificado do objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da91f-129">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="da91f-130">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="da91f-130">-RemoveProtectedItem</span></span>
<span data-ttu-id="da91f-131">Lista de itens protegidos de replicação ASR a serem removidos do grupo plano de recuperação no objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="da91f-131">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="da91f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da91f-132">-WhatIf</span></span>
<span data-ttu-id="da91f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da91f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da91f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da91f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da91f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da91f-135">CommonParameters</span></span>
<span data-ttu-id="da91f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da91f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da91f-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da91f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da91f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da91f-138">INPUTS</span></span>

### <span data-ttu-id="da91f-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da91f-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="da91f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da91f-140">OUTPUTS</span></span>

### <span data-ttu-id="da91f-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="da91f-141">System.Object</span></span>

## <span data-ttu-id="da91f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da91f-142">NOTES</span></span>

## <span data-ttu-id="da91f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da91f-143">RELATED LINKS</span></span>

[<span data-ttu-id="da91f-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da91f-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="da91f-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="da91f-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
