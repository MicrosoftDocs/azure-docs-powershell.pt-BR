---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609895"
---
# <span data-ttu-id="51076-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="51076-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="51076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51076-102">SYNOPSIS</span></span>
<span data-ttu-id="51076-103">Inicia um trabalho de associação de política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="51076-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51076-104">SYNTAX</span></span>

### <span data-ttu-id="51076-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="51076-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51076-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="51076-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51076-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51076-107">DESCRIPTION</span></span>
<span data-ttu-id="51076-108">O cmdlet **Start-AzureRmSiteRecoveryPolicyAssociationJob** inicia um trabalho de associação para associar uma política de replicação a um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="51076-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="51076-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51076-109">EXAMPLES</span></span>

## <span data-ttu-id="51076-110">OS</span><span class="sxs-lookup"><span data-stu-id="51076-110">PARAMETERS</span></span>

### <span data-ttu-id="51076-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51076-111">-DefaultProfile</span></span>
<span data-ttu-id="51076-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51076-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51076-113">-Política</span><span class="sxs-lookup"><span data-stu-id="51076-113">-Policy</span></span>
<span data-ttu-id="51076-114">Especifica o objeto da política de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="51076-114">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51076-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="51076-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="51076-116">Especifica o contêiner de proteção principal no qual aplicar as configurações do perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="51076-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51076-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="51076-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="51076-118">Especifica o contêiner de proteção de recuperação no qual aplicar as configurações de perfil de proteção.</span><span class="sxs-lookup"><span data-stu-id="51076-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51076-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51076-119">CommonParameters</span></span>
<span data-ttu-id="51076-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51076-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51076-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51076-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51076-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51076-122">INPUTS</span></span>

### <span data-ttu-id="51076-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="51076-123">ASRPolicy</span></span>
<span data-ttu-id="51076-124">O parâmetro "política" aceita o valor do tipo "ASRPolicy" da pipeline</span><span class="sxs-lookup"><span data-stu-id="51076-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="51076-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51076-125">OUTPUTS</span></span>

### <span data-ttu-id="51076-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51076-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51076-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51076-127">NOTES</span></span>

## <span data-ttu-id="51076-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51076-128">RELATED LINKS</span></span>

