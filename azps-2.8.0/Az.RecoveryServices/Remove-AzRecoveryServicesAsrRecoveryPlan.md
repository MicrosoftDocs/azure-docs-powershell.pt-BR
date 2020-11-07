---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4931b32cf2c74180ad06b071d19ef57f4be2285e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772970"
---
# <span data-ttu-id="f10f6-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10f6-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f10f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f10f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f10f6-103">Exclui o plano de recuperação ASR especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f10f6-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="f10f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f10f6-104">SYNTAX</span></span>

### <span data-ttu-id="f10f6-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="f10f6-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f10f6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f10f6-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f10f6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f10f6-107">DESCRIPTION</span></span>
<span data-ttu-id="f10f6-108">O cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** exclui o plano de recuperação especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f10f6-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="f10f6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f10f6-109">EXAMPLES</span></span>

### <span data-ttu-id="f10f6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f10f6-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f10f6-111">Inicia a exclusão do plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="f10f6-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f10f6-112">OS</span><span class="sxs-lookup"><span data-stu-id="f10f6-112">PARAMETERS</span></span>

### <span data-ttu-id="f10f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10f6-113">-DefaultProfile</span></span>
<span data-ttu-id="f10f6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f10f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f10f6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f10f6-115">-InputObject</span></span>
<span data-ttu-id="f10f6-116">O objeto de entrada para o cmdlet: o objeto do plano de recuperação ASR correspondente ao plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f10f6-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="f10f6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f10f6-117">-Name</span></span>
<span data-ttu-id="f10f6-118">Especifica o nome do plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f10f6-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="f10f6-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f10f6-119">-Confirm</span></span>
<span data-ttu-id="f10f6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f10f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f10f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f10f6-121">-WhatIf</span></span>
<span data-ttu-id="f10f6-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f10f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f10f6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f10f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f10f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10f6-124">CommonParameters</span></span>
<span data-ttu-id="f10f6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f10f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10f6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10f6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f10f6-127">INPUTS</span></span>

### <span data-ttu-id="f10f6-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10f6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f10f6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f10f6-129">OUTPUTS</span></span>

### <span data-ttu-id="f10f6-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f10f6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f10f6-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f10f6-131">NOTES</span></span>

## <span data-ttu-id="f10f6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f10f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="f10f6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10f6-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f10f6-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10f6-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f10f6-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10f6-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

