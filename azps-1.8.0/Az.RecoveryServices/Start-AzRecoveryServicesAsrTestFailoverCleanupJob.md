---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599596"
---
# <span data-ttu-id="22047-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="22047-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="22047-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22047-102">SYNOPSIS</span></span>
<span data-ttu-id="22047-103">Inicia a operação de limpeza do failover de teste.</span><span class="sxs-lookup"><span data-stu-id="22047-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="22047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22047-104">SYNTAX</span></span>

### <span data-ttu-id="22047-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="22047-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22047-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="22047-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22047-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="22047-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22047-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22047-108">DESCRIPTION</span></span>
<span data-ttu-id="22047-109">O cmdlet **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** inicia a operação de limpeza de failover de teste em um item ou plano de recuperação de replicação no qual um failover de teste foi executado.</span><span class="sxs-lookup"><span data-stu-id="22047-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="22047-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22047-110">EXAMPLES</span></span>

### <span data-ttu-id="22047-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22047-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="22047-112">Trabalho para acompanhar a limpeza do failover de teste de um item protegido de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="22047-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="22047-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22047-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="22047-114">Trabalho para acompanhar a limpeza de failover de teste de um recoveryPlan de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="22047-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="22047-115">OS</span><span class="sxs-lookup"><span data-stu-id="22047-115">PARAMETERS</span></span>

### <span data-ttu-id="22047-116">-Comentário</span><span class="sxs-lookup"><span data-stu-id="22047-116">-Comment</span></span>
<span data-ttu-id="22047-117">Comentário do usuário para failover de teste.</span><span class="sxs-lookup"><span data-stu-id="22047-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22047-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22047-118">-DefaultProfile</span></span>
<span data-ttu-id="22047-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22047-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22047-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22047-120">-RecoveryPlan</span></span>
<span data-ttu-id="22047-121">Plano de recuperação para executar a limpeza de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="22047-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="22047-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22047-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="22047-123">Item protegido de replicação para executar a limpeza de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="22047-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="22047-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22047-124">-ResourceId</span></span>
<span data-ttu-id="22047-125">ID do recurso do plano de recuperação/item protegido de replicação para failover de teste do cleaningup.</span><span class="sxs-lookup"><span data-stu-id="22047-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22047-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22047-126">-Confirm</span></span>
<span data-ttu-id="22047-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22047-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22047-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22047-128">-WhatIf</span></span>
<span data-ttu-id="22047-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22047-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22047-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22047-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22047-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22047-131">CommonParameters</span></span>
<span data-ttu-id="22047-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22047-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22047-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22047-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22047-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22047-134">INPUTS</span></span>

### <span data-ttu-id="22047-135">System. String</span><span class="sxs-lookup"><span data-stu-id="22047-135">System.String</span></span>

### <span data-ttu-id="22047-136">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22047-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="22047-137">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22047-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="22047-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22047-138">OUTPUTS</span></span>

### <span data-ttu-id="22047-139">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="22047-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22047-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22047-140">NOTES</span></span>

## <span data-ttu-id="22047-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22047-141">RELATED LINKS</span></span>
