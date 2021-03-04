---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b0780e4fb82a3e58e70f3a0bd64b5211ad07fd42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890356"
---
# <span data-ttu-id="26133-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26133-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="26133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26133-102">SYNOPSIS</span></span>
<span data-ttu-id="26133-103">Atualiza o conteúdo de um plano de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="26133-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="26133-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26133-104">SYNTAX</span></span>

### <span data-ttu-id="26133-105">ByRPObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26133-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26133-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="26133-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26133-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26133-107">DESCRIPTION</span></span>
<span data-ttu-id="26133-108">O cmdlet **Update-AzRecoveryServicesAsrRecoveryPlan** atualiza o conteúdo de um plano de recuperação usando o conteúdo do objeto do plano de recuperação ASR especificado ou do arquivo json de definição do plano de recuperação asR.</span><span class="sxs-lookup"><span data-stu-id="26133-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="26133-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26133-109">EXAMPLES</span></span>

### <span data-ttu-id="26133-110">Exemplo 1: atualizar um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="26133-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="26133-111">Inicie a operação de atualização de um plano de recuperação usando o conteúdo do objeto de plano de recuperação ASR especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="26133-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="26133-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26133-112">PARAMETERS</span></span>

### <span data-ttu-id="26133-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26133-113">-DefaultProfile</span></span>
<span data-ttu-id="26133-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26133-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="26133-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26133-115">-InputObject</span></span>
<span data-ttu-id="26133-116">Objeto de entrada para o cmdlet: especifica um objeto de plano de recuperação ASR, o conteúdo do qual são usados para atualizar o plano de recuperação referido pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="26133-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26133-117">-Path</span><span class="sxs-lookup"><span data-stu-id="26133-117">-Path</span></span>
<span data-ttu-id="26133-118">Especifica o caminho do arquivo json de definição de plano de recuperação usado para atualizar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="26133-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26133-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26133-119">-Confirm</span></span>
<span data-ttu-id="26133-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26133-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26133-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26133-121">-WhatIf</span></span>
<span data-ttu-id="26133-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26133-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26133-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26133-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26133-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26133-124">CommonParameters</span></span>
<span data-ttu-id="26133-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26133-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26133-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26133-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26133-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26133-127">INPUTS</span></span>

### <span data-ttu-id="26133-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26133-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="26133-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26133-129">OUTPUTS</span></span>

### <span data-ttu-id="26133-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="26133-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26133-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="26133-131">NOTES</span></span>

## <span data-ttu-id="26133-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26133-132">RELATED LINKS</span></span>

[<span data-ttu-id="26133-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26133-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="26133-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26133-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="26133-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26133-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
