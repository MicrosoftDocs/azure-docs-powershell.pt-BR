---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114035"
---
# <span data-ttu-id="63635-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="63635-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="63635-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63635-102">SYNOPSIS</span></span>
<span data-ttu-id="63635-103">Exclui a política de replicação ASR especificada do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="63635-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="63635-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63635-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63635-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="63635-105">DESCRIPTION</span></span>
<span data-ttu-id="63635-106">O cmdlet **Remove-AzRecoveryServicesAsrPolicy** excluiu a política de replicação especificada do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="63635-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="63635-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63635-107">EXAMPLES</span></span>

### <span data-ttu-id="63635-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63635-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="63635-109">Inicia a exclusão da política de replicação especificada e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="63635-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63635-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63635-110">PARAMETERS</span></span>

### <span data-ttu-id="63635-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63635-111">-DefaultProfile</span></span>
<span data-ttu-id="63635-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63635-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="63635-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63635-113">-InputObject</span></span>
<span data-ttu-id="63635-114">O objeto de entrada para o cmdlet: o objeto de política de replicação ASR correspondente à política de replicação a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="63635-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="63635-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="63635-115">-Confirm</span></span>
<span data-ttu-id="63635-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63635-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63635-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63635-117">-WhatIf</span></span>
<span data-ttu-id="63635-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="63635-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63635-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63635-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63635-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63635-120">CommonParameters</span></span>
<span data-ttu-id="63635-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63635-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63635-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63635-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63635-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="63635-123">INPUTS</span></span>

### <span data-ttu-id="63635-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="63635-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="63635-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="63635-125">OUTPUTS</span></span>

### <span data-ttu-id="63635-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="63635-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63635-127">Notas</span><span class="sxs-lookup"><span data-stu-id="63635-127">NOTES</span></span>

## <span data-ttu-id="63635-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63635-128">RELATED LINKS</span></span>

[<span data-ttu-id="63635-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="63635-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="63635-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="63635-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
