---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609586"
---
# <span data-ttu-id="9171b-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9171b-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="9171b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9171b-102">SYNOPSIS</span></span>
<span data-ttu-id="9171b-103">Atualiza (atualizar servidor) as informações recebidas do provedor de serviços de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9171b-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9171b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9171b-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9171b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9171b-105">DESCRIPTION</span></span>
<span data-ttu-id="9171b-106">O cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** atualiza as informações recebidas do provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9171b-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="9171b-107">Você pode usar esse cmdlet para disparar uma atualização das informações recebidas do provedor de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="9171b-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="9171b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9171b-108">EXAMPLES</span></span>

### <span data-ttu-id="9171b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9171b-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="9171b-110">Inicia a operação de atualização das informações do provedor de serviços ASR especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="9171b-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="9171b-111">OS</span><span class="sxs-lookup"><span data-stu-id="9171b-111">PARAMETERS</span></span>

### <span data-ttu-id="9171b-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9171b-112">-InputObject</span></span>
<span data-ttu-id="9171b-113">Objeto de entrada: especifica o objeto do provedor de serviços ASR correspondente ao provedor de serviços ASR que identifica o servidor para o qual as informações serão atualizadas (atualizadas.)</span><span class="sxs-lookup"><span data-stu-id="9171b-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="9171b-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9171b-114">-Confirm</span></span>
<span data-ttu-id="9171b-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9171b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9171b-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9171b-116">-WhatIf</span></span>
<span data-ttu-id="9171b-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9171b-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9171b-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9171b-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9171b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9171b-119">CommonParameters</span></span>
<span data-ttu-id="9171b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9171b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9171b-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9171b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9171b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9171b-122">INPUTS</span></span>

### <span data-ttu-id="9171b-123">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9171b-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="9171b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9171b-124">OUTPUTS</span></span>

### <span data-ttu-id="9171b-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="9171b-125">System.Object</span></span>

## <span data-ttu-id="9171b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9171b-126">NOTES</span></span>

## <span data-ttu-id="9171b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9171b-127">RELATED LINKS</span></span>

[<span data-ttu-id="9171b-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9171b-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="9171b-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9171b-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
