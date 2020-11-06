---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 5d0d6bc894cd252ac36b4ceee312040a998b3857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428833"
---
# <span data-ttu-id="eb644-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb644-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="eb644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb644-102">SYNOPSIS</span></span>
<span data-ttu-id="eb644-103">Obtém mapeamentos de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="eb644-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb644-104">SYNTAX</span></span>

### <span data-ttu-id="eb644-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb644-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb644-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="eb644-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb644-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb644-107">DESCRIPTION</span></span>
<span data-ttu-id="eb644-108">O cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política de replicação (Associação) no cofre para o contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="eb644-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="eb644-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb644-109">EXAMPLES</span></span>

### <span data-ttu-id="eb644-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb644-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="eb644-111">Lista de mapeamentos de contêineres de proteção para contêiner.</span><span class="sxs-lookup"><span data-stu-id="eb644-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="eb644-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb644-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="eb644-113">Obtém todos os mapeamentos de contêiner de proteção para o contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="eb644-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="eb644-114">OS</span><span class="sxs-lookup"><span data-stu-id="eb644-114">PARAMETERS</span></span>

### <span data-ttu-id="eb644-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb644-115">-DefaultProfile</span></span>
<span data-ttu-id="eb644-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb644-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="eb644-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb644-117">-Name</span></span>
<span data-ttu-id="eb644-118">Especifica o nome do mapeamento de contêiner de proteção a obter.</span><span class="sxs-lookup"><span data-stu-id="eb644-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb644-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eb644-119">-ProtectionContainer</span></span>
<span data-ttu-id="eb644-120">Obter mapeamentos de contêiner de proteção correspondentes ao objeto contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="eb644-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb644-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb644-121">CommonParameters</span></span>
<span data-ttu-id="eb644-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb644-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb644-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb644-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb644-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb644-124">INPUTS</span></span>

### <span data-ttu-id="eb644-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eb644-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="eb644-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb644-126">OUTPUTS</span></span>

### <span data-ttu-id="eb644-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eb644-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eb644-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb644-128">NOTES</span></span>

## <span data-ttu-id="eb644-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb644-129">RELATED LINKS</span></span>

[<span data-ttu-id="eb644-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb644-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="eb644-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb644-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
