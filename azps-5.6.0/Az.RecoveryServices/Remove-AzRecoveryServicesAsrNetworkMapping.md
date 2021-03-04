---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: bb80bebc8c1a5dccbeedf4abd277891c3b2e9de7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885546"
---
# <span data-ttu-id="9c5a2-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c5a2-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9c5a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5a2-103">Exclui o mapeamento de rede ASR especificado do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="9c5a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c5a2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c5a2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c5a2-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5a2-106">O cmdlet **Remove-AzRecoveryServicesAsrNetworkMapping** exclui o mapeamento de rede ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="9c5a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c5a2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="9c5a2-109">Inicia a exclusão do mapeamento de rede ASR especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9c5a2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-110">PARAMETERS</span></span>

### <span data-ttu-id="9c5a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5a2-111">-DefaultProfile</span></span>
<span data-ttu-id="9c5a2-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9c5a2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c5a2-113">-InputObject</span></span>
<span data-ttu-id="9c5a2-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c5a2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c5a2-115">-Confirm</span></span>
<span data-ttu-id="9c5a2-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5a2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5a2-117">-WhatIf</span></span>
<span data-ttu-id="9c5a2-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c5a2-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5a2-120">CommonParameters</span></span>
<span data-ttu-id="9c5a2-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5a2-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c5a2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5a2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-123">INPUTS</span></span>

### <span data-ttu-id="9c5a2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c5a2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="9c5a2-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-125">OUTPUTS</span></span>

### <span data-ttu-id="9c5a2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9c5a2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9c5a2-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c5a2-127">NOTES</span></span>

## <span data-ttu-id="9c5a2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c5a2-128">RELATED LINKS</span></span>

[<span data-ttu-id="9c5a2-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c5a2-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9c5a2-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c5a2-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
