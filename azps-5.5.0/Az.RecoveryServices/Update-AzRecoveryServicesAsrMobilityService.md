---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112683"
---
# <span data-ttu-id="7c485-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="7c485-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="7c485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c485-102">SYNOPSIS</span></span>
<span data-ttu-id="7c485-103">Atualizações do agente de serviço de mobilidade push para máquinas protegidas.</span><span class="sxs-lookup"><span data-stu-id="7c485-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="7c485-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c485-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c485-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c485-105">DESCRIPTION</span></span>
<span data-ttu-id="7c485-106">O cmdlet **Update-AzRecoveryServicesAsrMobilityService** tenta pressionar atualizações do agente de serviços de mobilidade para máquinas protegidas (se uma atualização estiver disponível.)</span><span class="sxs-lookup"><span data-stu-id="7c485-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="7c485-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c485-107">EXAMPLES</span></span>

### <span data-ttu-id="7c485-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c485-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="7c485-109">Trabalho para controlar o Agente de Serviço de Mobilidade do Item Protegido de Replicação de Atualização.</span><span class="sxs-lookup"><span data-stu-id="7c485-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="7c485-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c485-110">PARAMETERS</span></span>

### <span data-ttu-id="7c485-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="7c485-111">-Account</span></span>
<span data-ttu-id="7c485-112">A ID da conta a ser usada para pressionar a atualização.</span><span class="sxs-lookup"><span data-stu-id="7c485-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="7c485-113">Deve ser uma da lista de contas de executar como na tela ASR correspondente ao computador que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="7c485-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="7c485-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c485-114">-DefaultProfile</span></span>
<span data-ttu-id="7c485-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7c485-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c485-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c485-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7c485-117">Item protegido de replicação do Site do Azure a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="7c485-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="7c485-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7c485-118">-Confirm</span></span>
<span data-ttu-id="7c485-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c485-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c485-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c485-120">-WhatIf</span></span>
<span data-ttu-id="7c485-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7c485-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c485-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c485-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c485-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c485-123">CommonParameters</span></span>
<span data-ttu-id="7c485-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c485-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c485-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c485-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c485-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="7c485-126">INPUTS</span></span>

### <span data-ttu-id="7c485-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c485-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7c485-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="7c485-128">OUTPUTS</span></span>

### <span data-ttu-id="7c485-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7c485-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7c485-130">Notas</span><span class="sxs-lookup"><span data-stu-id="7c485-130">NOTES</span></span>

## <span data-ttu-id="7c485-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c485-131">RELATED LINKS</span></span>
