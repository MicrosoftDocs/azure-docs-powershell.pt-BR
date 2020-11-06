---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432545"
---
# <span data-ttu-id="81748-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81748-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="81748-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81748-102">SYNOPSIS</span></span>
<span data-ttu-id="81748-103">Cria um mapeamento de contêiner de proteção do Azure site Recovery ao associar uma política a um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="81748-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81748-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81748-104">SYNTAX</span></span>

### <span data-ttu-id="81748-105">EnterpriseToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="81748-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81748-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="81748-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81748-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81748-107">DESCRIPTION</span></span>
<span data-ttu-id="81748-108">O cmdlet **New-AzureRmSiteRecoveryProtectionContainerMapping** cria um mapeamento de contêiner de proteção do Azure site Recovery ao associar uma política a um contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="81748-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="81748-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81748-109">EXAMPLES</span></span>

## <span data-ttu-id="81748-110">OS</span><span class="sxs-lookup"><span data-stu-id="81748-110">PARAMETERS</span></span>

### <span data-ttu-id="81748-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="81748-111">-Name</span></span>
<span data-ttu-id="81748-112">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="81748-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81748-113">-Política</span><span class="sxs-lookup"><span data-stu-id="81748-113">-Policy</span></span>
<span data-ttu-id="81748-114">Especifica o objeto da política do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="81748-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="81748-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="81748-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="81748-116">Especifica o objeto do contêiner de proteção principal.</span><span class="sxs-lookup"><span data-stu-id="81748-116">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="81748-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="81748-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="81748-118">Especifica o objeto de contêiner da proteção de recuperação.</span><span class="sxs-lookup"><span data-stu-id="81748-118">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="81748-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81748-119">-DefaultProfile</span></span>
<span data-ttu-id="81748-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81748-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81748-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81748-121">CommonParameters</span></span>
<span data-ttu-id="81748-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81748-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81748-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81748-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81748-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81748-124">INPUTS</span></span>

### <span data-ttu-id="81748-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="81748-125">ASRPolicy</span></span>
<span data-ttu-id="81748-126">O parâmetro "política" aceita o valor do tipo "ASRPolicy" da pipeline</span><span class="sxs-lookup"><span data-stu-id="81748-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="81748-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81748-127">OUTPUTS</span></span>

### <span data-ttu-id="81748-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="81748-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81748-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81748-129">NOTES</span></span>

## <span data-ttu-id="81748-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81748-130">RELATED LINKS</span></span>

[<span data-ttu-id="81748-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81748-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="81748-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="81748-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
