---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610450"
---
# <span data-ttu-id="58eee-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="58eee-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="58eee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58eee-102">SYNOPSIS</span></span>
<span data-ttu-id="58eee-103">Cria um mapeamento entre redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="58eee-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58eee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58eee-104">SYNTAX</span></span>

### <span data-ttu-id="58eee-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="58eee-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58eee-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="58eee-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58eee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58eee-107">DESCRIPTION</span></span>
<span data-ttu-id="58eee-108">O cmdlet **New-AzureRMSiteRecoveryNetworkMapping** cria um mapeamento entre duas redes virtuais e retorna um trabalho do Azure site Recovery para controlá-la.</span><span class="sxs-lookup"><span data-stu-id="58eee-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="58eee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58eee-109">EXAMPLES</span></span>

## <span data-ttu-id="58eee-110">OS</span><span class="sxs-lookup"><span data-stu-id="58eee-110">PARAMETERS</span></span>

### <span data-ttu-id="58eee-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="58eee-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="58eee-112">Especifica a ID de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="58eee-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eee-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="58eee-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eee-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="58eee-114">-PrimaryNetwork</span></span>
<span data-ttu-id="58eee-115">Especifica o objeto de rede principal.</span><span class="sxs-lookup"><span data-stu-id="58eee-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58eee-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="58eee-116">-RecoveryNetwork</span></span>
<span data-ttu-id="58eee-117">Especifica o objeto de rede de recuperação.</span><span class="sxs-lookup"><span data-stu-id="58eee-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58eee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58eee-118">-DefaultProfile</span></span>
<span data-ttu-id="58eee-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58eee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58eee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58eee-120">CommonParameters</span></span>
<span data-ttu-id="58eee-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58eee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58eee-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58eee-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58eee-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58eee-123">INPUTS</span></span>

### <span data-ttu-id="58eee-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="58eee-124">ASRNetwork</span></span>
<span data-ttu-id="58eee-125">O parâmetro ' PrimaryNetwork ' aceita o valor do tipo ' ASRNetwork ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="58eee-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="58eee-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58eee-126">OUTPUTS</span></span>

### <span data-ttu-id="58eee-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58eee-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58eee-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58eee-128">NOTES</span></span>

## <span data-ttu-id="58eee-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58eee-129">RELATED LINKS</span></span>

[<span data-ttu-id="58eee-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="58eee-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="58eee-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="58eee-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
