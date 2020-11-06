---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429154"
---
# <span data-ttu-id="9c029-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c029-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9c029-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c029-102">SYNOPSIS</span></span>
<span data-ttu-id="9c029-103">Exclui o mapeamento de rede ASR especificado do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9c029-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c029-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c029-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c029-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c029-105">DESCRIPTION</span></span>
<span data-ttu-id="9c029-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** exclui o mapeamento de rede ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="9c029-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="9c029-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c029-107">EXAMPLES</span></span>

### <span data-ttu-id="9c029-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c029-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="9c029-109">Inicia a exclusão do mapeamento de rede ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9c029-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9c029-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c029-110">PARAMETERS</span></span>

### <span data-ttu-id="9c029-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c029-111">-InputObject</span></span>
<span data-ttu-id="9c029-112">O objeto de entrada para o cmdlet: o objeto de mapeamento de rede ASR correspondente ao mapeamento de rede ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9c029-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c029-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c029-113">-Confirm</span></span>
<span data-ttu-id="9c029-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c029-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c029-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c029-115">-WhatIf</span></span>
<span data-ttu-id="9c029-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c029-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c029-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c029-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c029-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c029-118">CommonParameters</span></span>
<span data-ttu-id="9c029-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c029-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c029-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c029-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c029-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c029-121">INPUTS</span></span>

### <span data-ttu-id="9c029-122">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c029-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="9c029-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c029-123">OUTPUTS</span></span>

### <span data-ttu-id="9c029-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9c029-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9c029-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c029-125">NOTES</span></span>

## <span data-ttu-id="9c029-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c029-126">RELATED LINKS</span></span>

[<span data-ttu-id="9c029-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c029-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9c029-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9c029-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
