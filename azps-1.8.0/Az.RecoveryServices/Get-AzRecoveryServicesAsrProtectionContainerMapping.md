---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 588c00dc877c4e451a4d8a0c0b44ec001b0787ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599730"
---
# <span data-ttu-id="d2182-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d2182-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d2182-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2182-102">SYNOPSIS</span></span>
<span data-ttu-id="d2182-103">Obtém mapeamentos de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d2182-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="d2182-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2182-104">SYNTAX</span></span>

### <span data-ttu-id="d2182-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2182-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2182-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d2182-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2182-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2182-107">DESCRIPTION</span></span>
<span data-ttu-id="d2182-108">O cmdlet **Get-AzRecoveryServicesAsrProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política de replicação (Associação) no cofre para o contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="d2182-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="d2182-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2182-109">EXAMPLES</span></span>

### <span data-ttu-id="d2182-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2182-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="d2182-111">Lista de mapeamentos de contêineres de proteção para contêiner.</span><span class="sxs-lookup"><span data-stu-id="d2182-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="d2182-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2182-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

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

<span data-ttu-id="d2182-113">Obtém todos os mapeamentos de contêiner de proteção para o contêiner de proteção especificado.</span><span class="sxs-lookup"><span data-stu-id="d2182-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="d2182-114">OS</span><span class="sxs-lookup"><span data-stu-id="d2182-114">PARAMETERS</span></span>

### <span data-ttu-id="d2182-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2182-115">-DefaultProfile</span></span>
<span data-ttu-id="d2182-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2182-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2182-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2182-117">-Name</span></span>
<span data-ttu-id="d2182-118">Especifica o nome do mapeamento de contêiner de proteção a obter.</span><span class="sxs-lookup"><span data-stu-id="d2182-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2182-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d2182-119">-ProtectionContainer</span></span>
<span data-ttu-id="d2182-120">Obter mapeamentos de contêiner de proteção correspondentes ao objeto contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="d2182-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2182-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2182-121">CommonParameters</span></span>
<span data-ttu-id="d2182-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2182-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2182-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2182-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2182-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2182-124">INPUTS</span></span>

### <span data-ttu-id="d2182-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d2182-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d2182-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2182-126">OUTPUTS</span></span>

### <span data-ttu-id="d2182-127">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d2182-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="d2182-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2182-128">NOTES</span></span>

## <span data-ttu-id="d2182-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2182-129">RELATED LINKS</span></span>

[<span data-ttu-id="d2182-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d2182-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d2182-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d2182-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
