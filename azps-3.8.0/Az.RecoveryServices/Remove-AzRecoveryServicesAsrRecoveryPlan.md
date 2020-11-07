---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942639"
---
# <span data-ttu-id="b12c0-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b12c0-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b12c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b12c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b12c0-103">Exclui o plano de recuperação ASR especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b12c0-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="b12c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b12c0-104">SYNTAX</span></span>

### <span data-ttu-id="b12c0-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="b12c0-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12c0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b12c0-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b12c0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b12c0-107">DESCRIPTION</span></span>
<span data-ttu-id="b12c0-108">O cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** exclui o plano de recuperação especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b12c0-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="b12c0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b12c0-109">EXAMPLES</span></span>

### <span data-ttu-id="b12c0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b12c0-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="b12c0-111">Inicia a exclusão do plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b12c0-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b12c0-112">OS</span><span class="sxs-lookup"><span data-stu-id="b12c0-112">PARAMETERS</span></span>

### <span data-ttu-id="b12c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12c0-113">-DefaultProfile</span></span>
<span data-ttu-id="b12c0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b12c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b12c0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b12c0-115">-InputObject</span></span>
<span data-ttu-id="b12c0-116">O objeto de entrada para o cmdlet: o objeto do plano de recuperação ASR correspondente ao plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b12c0-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b12c0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b12c0-117">-Name</span></span>
<span data-ttu-id="b12c0-118">Especifica o nome do plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b12c0-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12c0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b12c0-119">-Confirm</span></span>
<span data-ttu-id="b12c0-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b12c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b12c0-121">-WhatIf</span></span>
<span data-ttu-id="b12c0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b12c0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b12c0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b12c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b12c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12c0-124">CommonParameters</span></span>
<span data-ttu-id="b12c0-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b12c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12c0-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b12c0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12c0-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b12c0-127">INPUTS</span></span>

### <span data-ttu-id="b12c0-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b12c0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="b12c0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b12c0-129">OUTPUTS</span></span>

### <span data-ttu-id="b12c0-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b12c0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b12c0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b12c0-131">NOTES</span></span>

## <span data-ttu-id="b12c0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b12c0-132">RELATED LINKS</span></span>

[<span data-ttu-id="b12c0-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b12c0-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b12c0-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b12c0-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b12c0-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b12c0-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


