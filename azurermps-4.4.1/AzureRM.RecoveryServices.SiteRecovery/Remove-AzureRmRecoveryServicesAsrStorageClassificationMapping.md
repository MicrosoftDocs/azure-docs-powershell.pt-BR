---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433039"
---
# <span data-ttu-id="993fe-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="993fe-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="993fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="993fe-102">SYNOPSIS</span></span>
<span data-ttu-id="993fe-103">Exclui o mapeamento de classificação de armazenamento ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="993fe-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="993fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="993fe-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="993fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="993fe-105">DESCRIPTION</span></span>
<span data-ttu-id="993fe-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** exclui o mapeamento de classificação de armazenamento do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="993fe-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="993fe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="993fe-107">EXAMPLES</span></span>

### <span data-ttu-id="993fe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="993fe-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="993fe-109">Inicia a exclusão do mapeamento de classificação de armazenamento especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="993fe-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="993fe-110">OS</span><span class="sxs-lookup"><span data-stu-id="993fe-110">PARAMETERS</span></span>

### <span data-ttu-id="993fe-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="993fe-111">-InputObject</span></span>
<span data-ttu-id="993fe-112">O objeto de entrada para o cmdlet: o objeto de mapeamento de classificação de armazenamento ASR correspondente ao mapeamento de classificação de armazenamento ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="993fe-112">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="993fe-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="993fe-113">-Confirm</span></span>
<span data-ttu-id="993fe-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="993fe-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993fe-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993fe-115">-WhatIf</span></span>
<span data-ttu-id="993fe-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="993fe-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="993fe-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="993fe-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993fe-118">CommonParameters</span></span>
<span data-ttu-id="993fe-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993fe-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="993fe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993fe-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="993fe-121">INPUTS</span></span>

### <span data-ttu-id="993fe-122">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="993fe-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="993fe-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="993fe-123">OUTPUTS</span></span>

### <span data-ttu-id="993fe-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="993fe-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="993fe-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="993fe-125">NOTES</span></span>

## <span data-ttu-id="993fe-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="993fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="993fe-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="993fe-127">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="993fe-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="993fe-128">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
