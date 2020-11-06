---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440969"
---
# <span data-ttu-id="522d1-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="522d1-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="522d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="522d1-102">SYNOPSIS</span></span>
<span data-ttu-id="522d1-103">Exclui/cancela o registro do provedor de serviços de recuperação do Azure site Recovery especificado no cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="522d1-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="522d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="522d1-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="522d1-105">DESCRIPTION</span></span>
<span data-ttu-id="522d1-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** remove o provedor de serviços de recuperação do Azure site Recovery especificado do cofre.</span><span class="sxs-lookup"><span data-stu-id="522d1-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="522d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="522d1-107">EXAMPLES</span></span>

### <span data-ttu-id="522d1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="522d1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="522d1-109">Inicia a exclusão/cancelamento de registro do provedor de serviços de recuperação de site do Azure especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="522d1-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="522d1-110">OS</span><span class="sxs-lookup"><span data-stu-id="522d1-110">PARAMETERS</span></span>

### <span data-ttu-id="522d1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="522d1-111">-Force</span></span>
<span data-ttu-id="522d1-112">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="522d1-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="522d1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="522d1-113">-InputObject</span></span>
<span data-ttu-id="522d1-114">O objeto de entrada para o cmdlet: o objeto do provedor de serviços de recuperação ASR correspondente ao provedor de serviços de recuperação ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="522d1-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522d1-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="522d1-115">-Confirm</span></span>
<span data-ttu-id="522d1-116">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="522d1-116">Specify if confirmation is required.</span></span> <span data-ttu-id="522d1-117">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="522d1-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="522d1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522d1-118">-WhatIf</span></span>
<span data-ttu-id="522d1-119">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="522d1-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="522d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522d1-120">CommonParameters</span></span>
<span data-ttu-id="522d1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522d1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522d1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522d1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="522d1-123">INPUTS</span></span>

### <span data-ttu-id="522d1-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="522d1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="522d1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="522d1-125">OUTPUTS</span></span>

### <span data-ttu-id="522d1-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="522d1-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="522d1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="522d1-127">NOTES</span></span>

## <span data-ttu-id="522d1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="522d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="522d1-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="522d1-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="522d1-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="522d1-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
