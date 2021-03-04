---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885529"
---
# <span data-ttu-id="6f694-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6f694-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="6f694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f694-102">SYNOPSIS</span></span>
<span data-ttu-id="6f694-103">Exclui/não registro do provedor de serviços de recuperação de site especificado do Azure Site Recovery do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="6f694-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="6f694-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f694-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f694-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f694-105">DESCRIPTION</span></span>
<span data-ttu-id="6f694-106">O cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** remove o provedor de serviços de recuperação de site especificado do Azure Site Recovery do cofre.</span><span class="sxs-lookup"><span data-stu-id="6f694-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="6f694-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f694-107">EXAMPLES</span></span>

### <span data-ttu-id="6f694-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f694-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="6f694-109">Inicia a exclusão/não assinatura do provedor de serviços de Recuperação de Site especificado do Azure e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="6f694-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6f694-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f694-110">PARAMETERS</span></span>

### <span data-ttu-id="6f694-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f694-111">-DefaultProfile</span></span>
<span data-ttu-id="6f694-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f694-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6f694-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6f694-113">-Force</span></span>
<span data-ttu-id="6f694-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="6f694-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f694-115">-InputObject</span></span>
<span data-ttu-id="6f694-116">O objeto de entrada para o cmdlet: o objeto provedor de serviços de recuperação ASR correspondente ao provedor de serviços de recuperação ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6f694-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f694-117">-Confirm</span></span>
<span data-ttu-id="6f694-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="6f694-118">Specify if confirmation is required.</span></span> <span data-ttu-id="6f694-119">De definir o valor do parâmetro confirme como $false para ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6f694-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="6f694-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f694-120">-WhatIf</span></span>
<span data-ttu-id="6f694-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f694-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="6f694-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f694-122">CommonParameters</span></span>
<span data-ttu-id="6f694-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f694-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f694-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f694-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f694-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f694-125">INPUTS</span></span>

### <span data-ttu-id="6f694-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6f694-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="6f694-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f694-127">OUTPUTS</span></span>

### <span data-ttu-id="6f694-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6f694-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6f694-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f694-129">NOTES</span></span>

## <span data-ttu-id="6f694-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f694-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f694-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6f694-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="6f694-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6f694-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
