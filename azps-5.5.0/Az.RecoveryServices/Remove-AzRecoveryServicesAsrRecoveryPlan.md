---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118182"
---
# <span data-ttu-id="d6ae4-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6ae4-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="d6ae4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ae4-103">Exclui o plano de recuperação ASR especificado do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="d6ae4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6ae4-104">SYNTAX</span></span>

### <span data-ttu-id="d6ae4-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d6ae4-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ae4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d6ae4-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ae4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ae4-108">O cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** exclui o plano de recuperação especificado do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="d6ae4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6ae4-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ae4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6ae4-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="d6ae4-111">Inicia a exclusão do plano de recuperação especificado e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d6ae4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6ae4-112">PARAMETERS</span></span>

### <span data-ttu-id="d6ae4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ae4-113">-DefaultProfile</span></span>
<span data-ttu-id="d6ae4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d6ae4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6ae4-115">-InputObject</span></span>
<span data-ttu-id="d6ae4-116">O objeto de entrada para o cmdlet: o objeto do plano de recuperação ASR correspondente ao plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="d6ae4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6ae4-117">-Name</span></span>
<span data-ttu-id="d6ae4-118">Especifica o nome do plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="d6ae4-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d6ae4-119">-Confirm</span></span>
<span data-ttu-id="d6ae4-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ae4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ae4-121">-WhatIf</span></span>
<span data-ttu-id="d6ae4-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6ae4-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ae4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ae4-124">CommonParameters</span></span>
<span data-ttu-id="d6ae4-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ae4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ae4-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6ae4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ae4-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6ae4-127">INPUTS</span></span>

### <span data-ttu-id="d6ae4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6ae4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="d6ae4-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6ae4-129">OUTPUTS</span></span>

### <span data-ttu-id="d6ae4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6ae4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6ae4-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d6ae4-131">NOTES</span></span>

## <span data-ttu-id="d6ae4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6ae4-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6ae4-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6ae4-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d6ae4-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6ae4-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="d6ae4-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d6ae4-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


