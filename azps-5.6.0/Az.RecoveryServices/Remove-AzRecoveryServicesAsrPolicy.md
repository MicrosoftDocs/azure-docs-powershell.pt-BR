---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885545"
---
# <span data-ttu-id="bc6f6-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bc6f6-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="bc6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6f6-103">Exclui a política de replicação ASR especificada do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="bc6f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc6f6-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc6f6-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6f6-106">O cmdlet **Remove-AzRecoveryServicesAsrPolicy** excluiu a política de replicação especificada do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="bc6f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-107">EXAMPLES</span></span>

### <span data-ttu-id="bc6f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc6f6-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="bc6f6-109">Inicia a exclusão da política de replicação especificada e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bc6f6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-110">PARAMETERS</span></span>

### <span data-ttu-id="bc6f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6f6-111">-DefaultProfile</span></span>
<span data-ttu-id="bc6f6-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bc6f6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc6f6-113">-InputObject</span></span>
<span data-ttu-id="bc6f6-114">O objeto de entrada para o cmdlet: o objeto de política de replicação ASR correspondente à política de replicação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6f6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc6f6-115">-Confirm</span></span>
<span data-ttu-id="bc6f6-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6f6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6f6-117">-WhatIf</span></span>
<span data-ttu-id="bc6f6-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc6f6-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6f6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6f6-120">CommonParameters</span></span>
<span data-ttu-id="bc6f6-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6f6-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc6f6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6f6-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-123">INPUTS</span></span>

### <span data-ttu-id="bc6f6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="bc6f6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="bc6f6-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-125">OUTPUTS</span></span>

### <span data-ttu-id="bc6f6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bc6f6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bc6f6-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc6f6-127">NOTES</span></span>

## <span data-ttu-id="bc6f6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc6f6-128">RELATED LINKS</span></span>

[<span data-ttu-id="bc6f6-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bc6f6-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="bc6f6-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bc6f6-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
