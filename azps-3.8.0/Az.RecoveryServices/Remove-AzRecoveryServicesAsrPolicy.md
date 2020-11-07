---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942641"
---
# <span data-ttu-id="7e290-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7e290-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7e290-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e290-102">SYNOPSIS</span></span>
<span data-ttu-id="7e290-103">Exclui a política de replicação ASR especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7e290-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="7e290-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e290-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e290-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e290-105">DESCRIPTION</span></span>
<span data-ttu-id="7e290-106">O cmdlet **Remove-AzRecoveryServicesAsrPolicy** excluiu a política de replicação especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7e290-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="7e290-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e290-107">EXAMPLES</span></span>

### <span data-ttu-id="7e290-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e290-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="7e290-109">Inicia a exclusão da política de replicação especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="7e290-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7e290-110">OS</span><span class="sxs-lookup"><span data-stu-id="7e290-110">PARAMETERS</span></span>

### <span data-ttu-id="7e290-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e290-111">-DefaultProfile</span></span>
<span data-ttu-id="7e290-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e290-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7e290-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e290-113">-InputObject</span></span>
<span data-ttu-id="7e290-114">O objeto de entrada para o cmdlet: o objeto da política de replicação ASR correspondente à política de replicação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="7e290-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="7e290-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e290-115">-Confirm</span></span>
<span data-ttu-id="7e290-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e290-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e290-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e290-117">-WhatIf</span></span>
<span data-ttu-id="7e290-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e290-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e290-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e290-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e290-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e290-120">CommonParameters</span></span>
<span data-ttu-id="7e290-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e290-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e290-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e290-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e290-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e290-123">INPUTS</span></span>

### <span data-ttu-id="7e290-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="7e290-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="7e290-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e290-125">OUTPUTS</span></span>

### <span data-ttu-id="7e290-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7e290-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e290-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e290-127">NOTES</span></span>

## <span data-ttu-id="7e290-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e290-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e290-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7e290-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7e290-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7e290-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
