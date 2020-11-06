---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1e7e53d4f14649ac5cb8691a1e3d938809658771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609931"
---
# <span data-ttu-id="1cbae-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1cbae-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="1cbae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cbae-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbae-103">Obtém informações sobre mapeamentos de rede de recuperação de site para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="1cbae-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cbae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cbae-104">SYNTAX</span></span>

### <span data-ttu-id="1cbae-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cbae-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cbae-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1cbae-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cbae-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1cbae-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cbae-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="1cbae-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cbae-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="1cbae-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cbae-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cbae-110">DESCRIPTION</span></span>
<span data-ttu-id="1cbae-111">O cmdlet **Get-AzureRmSiteRecoveryNetworkMapping** Obtém informações sobre os mapeamentos de rede do Azure site Recovery para o cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="1cbae-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="1cbae-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cbae-112">EXAMPLES</span></span>

## <span data-ttu-id="1cbae-113">OS</span><span class="sxs-lookup"><span data-stu-id="1cbae-113">PARAMETERS</span></span>

### <span data-ttu-id="1cbae-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="1cbae-114">-Azure</span></span>
<span data-ttu-id="1cbae-115">Indica que o comando obtém uma lista de mapeamentos de rede para redes no servidor primário mapeado para redes virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbae-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbae-116">-DefaultProfile</span></span>
<span data-ttu-id="1cbae-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cbae-118">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="1cbae-118">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbae-119">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="1cbae-119">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbae-120">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="1cbae-120">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbae-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1cbae-121">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbae-122">CommonParameters</span></span>
<span data-ttu-id="1cbae-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbae-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbae-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cbae-125">INPUTS</span></span>

### <span data-ttu-id="1cbae-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1cbae-126">ASRFabric</span></span>
<span data-ttu-id="1cbae-127">O parâmetro ' PrimaryFabric ' aceita o valor do tipo ' ASRFabric ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1cbae-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="1cbae-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="1cbae-128">ASRServer</span></span>
<span data-ttu-id="1cbae-129">O parâmetro ' PrimaryServer ' aceita o valor do tipo ' ASRServer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1cbae-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="1cbae-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cbae-130">OUTPUTS</span></span>

### <span data-ttu-id="1cbae-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="1cbae-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="1cbae-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cbae-132">NOTES</span></span>

## <span data-ttu-id="1cbae-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cbae-133">RELATED LINKS</span></span>

[<span data-ttu-id="1cbae-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1cbae-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="1cbae-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1cbae-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
