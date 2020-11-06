---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 1e453f8b11929b96e6e0f2dbe96164c2bf351ae7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599602"
---
# <span data-ttu-id="16e2b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="16e2b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="16e2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="16e2b-103">Inicia a ação de failover de confirmação para um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="16e2b-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="16e2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16e2b-104">SYNTAX</span></span>

### <span data-ttu-id="16e2b-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="16e2b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e2b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="16e2b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e2b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16e2b-107">DESCRIPTION</span></span>
<span data-ttu-id="16e2b-108">O cmdlet **Start-AzRecoveryServicesAsrCommitFailoverJob** inicia o processo de failover de confirmação para um objeto do Azure site Recovery após uma operação de failover.</span><span class="sxs-lookup"><span data-stu-id="16e2b-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="16e2b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16e2b-109">EXAMPLES</span></span>

### <span data-ttu-id="16e2b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16e2b-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="16e2b-111">Inicia o failover de confirmação para o plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="16e2b-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="16e2b-112">OS</span><span class="sxs-lookup"><span data-stu-id="16e2b-112">PARAMETERS</span></span>

### <span data-ttu-id="16e2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e2b-113">-DefaultProfile</span></span>
<span data-ttu-id="16e2b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16e2b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="16e2b-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e2b-115">-RecoveryPlan</span></span>
<span data-ttu-id="16e2b-116">Especifica um objeto de plano de recuperação ASR correspondente ao plano de recuperação a ser failover.</span><span class="sxs-lookup"><span data-stu-id="16e2b-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e2b-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="16e2b-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="16e2b-118">Especifica um objeto de item protegido de replicação ASR correspondente ao item protegido de replicação para failover.</span><span class="sxs-lookup"><span data-stu-id="16e2b-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e2b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16e2b-119">-Confirm</span></span>
<span data-ttu-id="16e2b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e2b-121">-WhatIf</span></span>
<span data-ttu-id="16e2b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16e2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e2b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16e2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e2b-124">CommonParameters</span></span>
<span data-ttu-id="16e2b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e2b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e2b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16e2b-127">INPUTS</span></span>

### <span data-ttu-id="16e2b-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="16e2b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="16e2b-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="16e2b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="16e2b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16e2b-130">OUTPUTS</span></span>

### <span data-ttu-id="16e2b-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="16e2b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="16e2b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16e2b-132">NOTES</span></span>

## <span data-ttu-id="16e2b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e2b-133">RELATED LINKS</span></span>
