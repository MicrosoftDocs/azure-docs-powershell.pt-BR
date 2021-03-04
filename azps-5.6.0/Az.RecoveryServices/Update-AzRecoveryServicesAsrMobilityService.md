---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 5c5c9509c7ae242f98c8474a2ab87635f94dd62d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887682"
---
# <span data-ttu-id="79c52-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="79c52-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="79c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c52-102">SYNOPSIS</span></span>
<span data-ttu-id="79c52-103">Atualizações do agente de serviço de mobilidade por push para máquinas protegidas.</span><span class="sxs-lookup"><span data-stu-id="79c52-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="79c52-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79c52-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c52-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79c52-105">DESCRIPTION</span></span>
<span data-ttu-id="79c52-106">O cmdlet **Update-AzRecoveryServicesAsrMobilityService** tenta empurrar atualizações do agente de serviço de mobilidade para máquinas protegidas (se uma atualização estiver disponível.)</span><span class="sxs-lookup"><span data-stu-id="79c52-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="79c52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79c52-107">EXAMPLES</span></span>

### <span data-ttu-id="79c52-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79c52-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="79c52-109">Trabalho para rastrear o Agente de Serviço de Mobilidade do Item Protegido de Atualização.</span><span class="sxs-lookup"><span data-stu-id="79c52-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="79c52-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79c52-110">PARAMETERS</span></span>

### <span data-ttu-id="79c52-111">-Account</span><span class="sxs-lookup"><span data-stu-id="79c52-111">-Account</span></span>
<span data-ttu-id="79c52-112">A ID da conta a ser usada para pressionar a atualização.</span><span class="sxs-lookup"><span data-stu-id="79c52-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="79c52-113">Deve ser uma da lista de contas de executar como no tecido ASR correspondente ao computador que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="79c52-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c52-114">-DefaultProfile</span></span>
<span data-ttu-id="79c52-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="79c52-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c52-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79c52-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="79c52-117">Item protegido de replicação de recuperação de site do Azure a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="79c52-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c52-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79c52-118">-Confirm</span></span>
<span data-ttu-id="79c52-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c52-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c52-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c52-120">-WhatIf</span></span>
<span data-ttu-id="79c52-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79c52-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79c52-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79c52-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c52-123">CommonParameters</span></span>
<span data-ttu-id="79c52-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c52-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c52-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c52-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79c52-126">INPUTS</span></span>

### <span data-ttu-id="79c52-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79c52-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="79c52-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79c52-128">OUTPUTS</span></span>

### <span data-ttu-id="79c52-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="79c52-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79c52-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="79c52-130">NOTES</span></span>

## <span data-ttu-id="79c52-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79c52-131">RELATED LINKS</span></span>
