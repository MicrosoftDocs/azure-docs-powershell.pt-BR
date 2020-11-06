---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610260"
---
# <span data-ttu-id="b8ee4-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8ee4-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b8ee4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ee4-103">Exclui a política de replicação ASR especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ee4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8ee4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8ee4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ee4-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrPolicy** excluiu a política de replicação especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="b8ee4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="b8ee4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8ee4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="b8ee4-109">Inicia a exclusão da política de replicação especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b8ee4-110">OS</span><span class="sxs-lookup"><span data-stu-id="b8ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="b8ee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ee4-111">-DefaultProfile</span></span>
<span data-ttu-id="b8ee4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b8ee4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8ee4-113">-InputObject</span></span>
<span data-ttu-id="b8ee4-114">O objeto de entrada para o cmdlet: o objeto da política de replicação ASR correspondente à política de replicação a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="b8ee4-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8ee4-115">-Confirm</span></span>
<span data-ttu-id="b8ee4-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ee4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ee4-117">-WhatIf</span></span>
<span data-ttu-id="b8ee4-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8ee4-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ee4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ee4-120">CommonParameters</span></span>
<span data-ttu-id="b8ee4-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ee4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ee4-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ee4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ee4-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8ee4-123">INPUTS</span></span>

### <span data-ttu-id="b8ee4-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b8ee4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="b8ee4-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8ee4-125">OUTPUTS</span></span>

### <span data-ttu-id="b8ee4-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="b8ee4-126">System.Object</span></span>

## <span data-ttu-id="b8ee4-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8ee4-127">NOTES</span></span>

## <span data-ttu-id="b8ee4-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8ee4-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8ee4-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8ee4-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="b8ee4-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8ee4-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
