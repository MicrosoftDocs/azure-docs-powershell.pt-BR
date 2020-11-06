---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603339"
---
# <span data-ttu-id="6f1fb-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6f1fb-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="6f1fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1fb-103">Exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f1fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f1fb-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f1fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6f1fb-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** exclui o mapeamento de contêiner da proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="6f1fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f1fb-107">EXAMPLES</span></span>

### <span data-ttu-id="6f1fb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f1fb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="6f1fb-109">Inicia a exclusão do mapeamento de contêiner de proteção especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6f1fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="6f1fb-110">PARAMETERS</span></span>

### <span data-ttu-id="6f1fb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6f1fb-111">-Force</span></span>
<span data-ttu-id="6f1fb-112">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1fb-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1fb-113">-InputObject</span></span>
<span data-ttu-id="6f1fb-114">O objeto de entrada para o cmdlet: o objeto de mapeamento do contêiner de proteção ASR correspondente ao contêiner de proteção a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-114">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1fb-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f1fb-115">-Confirm</span></span>
<span data-ttu-id="6f1fb-116">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-116">Specify if confirmation is required.</span></span> <span data-ttu-id="6f1fb-117">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação</span><span class="sxs-lookup"><span data-stu-id="6f1fb-117">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="6f1fb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1fb-118">-WhatIf</span></span>
<span data-ttu-id="6f1fb-119">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="6f1fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1fb-120">CommonParameters</span></span>
<span data-ttu-id="6f1fb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1fb-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1fb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1fb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f1fb-123">INPUTS</span></span>

### <span data-ttu-id="6f1fb-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6f1fb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="6f1fb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f1fb-125">OUTPUTS</span></span>

### <span data-ttu-id="6f1fb-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6f1fb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6f1fb-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f1fb-127">NOTES</span></span>

## <span data-ttu-id="6f1fb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f1fb-128">RELATED LINKS</span></span>

[<span data-ttu-id="6f1fb-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6f1fb-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="6f1fb-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6f1fb-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
