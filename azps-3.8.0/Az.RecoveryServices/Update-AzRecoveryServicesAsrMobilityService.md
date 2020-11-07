---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943917"
---
# <span data-ttu-id="69e99-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="69e99-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="69e99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69e99-102">SYNOPSIS</span></span>
<span data-ttu-id="69e99-103">Atualizações do agente de serviço de mobilidade por push para computadores protegidos.</span><span class="sxs-lookup"><span data-stu-id="69e99-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="69e99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69e99-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69e99-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69e99-105">DESCRIPTION</span></span>
<span data-ttu-id="69e99-106">O cmdlet **Update-AzRecoveryServicesAsrMobilityService** tenta enviar por push atualizações de agente de serviço de mobilidade para computadores protegidos (se houver uma atualização disponível.)</span><span class="sxs-lookup"><span data-stu-id="69e99-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="69e99-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69e99-107">EXAMPLES</span></span>

### <span data-ttu-id="69e99-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69e99-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="69e99-109">Trabalho para acompanhar o agente de serviço de mobilidade do item protegido da replicação de atualização.</span><span class="sxs-lookup"><span data-stu-id="69e99-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="69e99-110">OS</span><span class="sxs-lookup"><span data-stu-id="69e99-110">PARAMETERS</span></span>

### <span data-ttu-id="69e99-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="69e99-111">-Account</span></span>
<span data-ttu-id="69e99-112">A ID da conta Executar como a ser usada para enviar a atualização.</span><span class="sxs-lookup"><span data-stu-id="69e99-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="69e99-113">Deve ser um na lista de contas Executar como da malha ASR correspondente ao computador que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="69e99-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="69e99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e99-114">-DefaultProfile</span></span>
<span data-ttu-id="69e99-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69e99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69e99-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69e99-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="69e99-117">Item protegido de replicação do Azure site Recovery a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="69e99-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="69e99-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69e99-118">-Confirm</span></span>
<span data-ttu-id="69e99-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69e99-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e99-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e99-120">-WhatIf</span></span>
<span data-ttu-id="69e99-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69e99-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69e99-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69e99-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e99-123">CommonParameters</span></span>
<span data-ttu-id="69e99-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e99-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69e99-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e99-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69e99-126">INPUTS</span></span>

### <span data-ttu-id="69e99-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="69e99-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="69e99-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69e99-128">OUTPUTS</span></span>

### <span data-ttu-id="69e99-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="69e99-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="69e99-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69e99-130">NOTES</span></span>

## <span data-ttu-id="69e99-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69e99-131">RELATED LINKS</span></span>
