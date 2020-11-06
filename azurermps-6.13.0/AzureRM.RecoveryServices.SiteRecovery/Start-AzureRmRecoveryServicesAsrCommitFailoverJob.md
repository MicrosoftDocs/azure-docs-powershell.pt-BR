---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427206"
---
# <span data-ttu-id="1b423-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1b423-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="1b423-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b423-102">SYNOPSIS</span></span>
<span data-ttu-id="1b423-103">Inicia a ação de failover de confirmação para um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="1b423-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b423-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b423-104">SYNTAX</span></span>

### <span data-ttu-id="1b423-105">ByRPIObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b423-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b423-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1b423-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b423-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b423-107">DESCRIPTION</span></span>
<span data-ttu-id="1b423-108">O cmdlet **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** inicia o processo de failover de confirmação para um objeto do Azure site Recovery após uma operação de failover.</span><span class="sxs-lookup"><span data-stu-id="1b423-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="1b423-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b423-109">EXAMPLES</span></span>

### <span data-ttu-id="1b423-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b423-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="1b423-111">Inicia o failover de confirmação para o plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="1b423-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1b423-112">OS</span><span class="sxs-lookup"><span data-stu-id="1b423-112">PARAMETERS</span></span>

### <span data-ttu-id="1b423-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b423-113">-DefaultProfile</span></span>
<span data-ttu-id="1b423-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b423-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1b423-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1b423-115">-RecoveryPlan</span></span>
<span data-ttu-id="1b423-116">Especifica um objeto de plano de recuperação ASR correspondente ao plano de recuperação a ser failover.</span><span class="sxs-lookup"><span data-stu-id="1b423-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="1b423-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b423-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1b423-118">Especifica um objeto de item protegido de replicação ASR correspondente ao item protegido de replicação para failover.</span><span class="sxs-lookup"><span data-stu-id="1b423-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="1b423-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b423-119">-Confirm</span></span>
<span data-ttu-id="1b423-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b423-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b423-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b423-121">-WhatIf</span></span>
<span data-ttu-id="1b423-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b423-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b423-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b423-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b423-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b423-124">CommonParameters</span></span>
<span data-ttu-id="1b423-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b423-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b423-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b423-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b423-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b423-127">INPUTS</span></span>

### <span data-ttu-id="1b423-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1b423-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="1b423-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1b423-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1b423-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b423-130">OUTPUTS</span></span>

### <span data-ttu-id="1b423-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1b423-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1b423-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b423-132">NOTES</span></span>

## <span data-ttu-id="1b423-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b423-133">RELATED LINKS</span></span>
