---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429060"
---
# <span data-ttu-id="a3882-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="a3882-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="a3882-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3882-102">SYNOPSIS</span></span>
<span data-ttu-id="a3882-103">Inicia um trabalho de dissociação em uma política de replicação associada a um contêiner de proteção de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="a3882-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3882-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3882-104">SYNTAX</span></span>

### <span data-ttu-id="a3882-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3882-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3882-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a3882-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3882-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3882-107">DESCRIPTION</span></span>
<span data-ttu-id="a3882-108">O cmdlet **Start-AzureRmSiteRecoveryPolicyDissociationJob** inicia um trabalho de dissociação na política de replicação associada a um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a3882-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="a3882-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3882-109">EXAMPLES</span></span>

## <span data-ttu-id="a3882-110">OS</span><span class="sxs-lookup"><span data-stu-id="a3882-110">PARAMETERS</span></span>

### <span data-ttu-id="a3882-111">-Política</span><span class="sxs-lookup"><span data-stu-id="a3882-111">-Policy</span></span>
<span data-ttu-id="a3882-112">Especifica um objeto de política de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3882-112">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3882-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a3882-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a3882-114">Especifica um contêiner de proteção principal.</span><span class="sxs-lookup"><span data-stu-id="a3882-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3882-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a3882-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a3882-116">Especifica um contêiner de proteção de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a3882-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3882-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3882-117">-DefaultProfile</span></span>
<span data-ttu-id="a3882-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3882-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3882-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3882-119">CommonParameters</span></span>
<span data-ttu-id="a3882-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3882-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3882-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3882-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3882-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3882-122">INPUTS</span></span>

### <span data-ttu-id="a3882-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a3882-123">ASRPolicy</span></span>
<span data-ttu-id="a3882-124">O parâmetro "política" aceita o valor do tipo "ASRPolicy" da pipeline</span><span class="sxs-lookup"><span data-stu-id="a3882-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="a3882-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3882-125">OUTPUTS</span></span>

### <span data-ttu-id="a3882-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a3882-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3882-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3882-127">NOTES</span></span>

## <span data-ttu-id="a3882-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3882-128">RELATED LINKS</span></span>

