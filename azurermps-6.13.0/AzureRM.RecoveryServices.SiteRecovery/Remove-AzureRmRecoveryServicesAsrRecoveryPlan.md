---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602104"
---
# <span data-ttu-id="b9e22-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b9e22-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b9e22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9e22-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e22-103">Exclui o plano de recuperação ASR especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b9e22-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9e22-104">SYNTAX</span></span>

### <span data-ttu-id="b9e22-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9e22-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e22-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b9e22-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e22-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9e22-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e22-108">O cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** exclui o plano de recuperação especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b9e22-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="b9e22-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e22-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e22-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9e22-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="b9e22-111">Inicia a exclusão do plano de recuperação especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b9e22-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b9e22-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9e22-112">PARAMETERS</span></span>

### <span data-ttu-id="b9e22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e22-113">-DefaultProfile</span></span>
<span data-ttu-id="b9e22-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b9e22-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9e22-115">-InputObject</span></span>
<span data-ttu-id="b9e22-116">O objeto de entrada para o cmdlet: o objeto do plano de recuperação ASR correspondente ao plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b9e22-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="b9e22-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e22-117">-Name</span></span>
<span data-ttu-id="b9e22-118">Especifica o nome do plano de recuperação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="b9e22-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="b9e22-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9e22-119">-Confirm</span></span>
<span data-ttu-id="b9e22-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e22-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e22-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e22-121">-WhatIf</span></span>
<span data-ttu-id="b9e22-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9e22-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9e22-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9e22-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e22-124">CommonParameters</span></span>
<span data-ttu-id="b9e22-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e22-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e22-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e22-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9e22-127">INPUTS</span></span>

### <span data-ttu-id="b9e22-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b9e22-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="b9e22-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9e22-129">OUTPUTS</span></span>

### <span data-ttu-id="b9e22-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="b9e22-130">System.Object</span></span>

## <span data-ttu-id="b9e22-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9e22-131">NOTES</span></span>

## <span data-ttu-id="b9e22-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e22-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9e22-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b9e22-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b9e22-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b9e22-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b9e22-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b9e22-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


