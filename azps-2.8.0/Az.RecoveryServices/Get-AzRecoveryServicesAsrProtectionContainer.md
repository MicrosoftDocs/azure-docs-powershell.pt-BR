---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: e37a2c0acf1cf1fa750e62f26431272fcc70b767
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773042"
---
# <span data-ttu-id="c95ab-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c95ab-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c95ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c95ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c95ab-103">Obtém contêineres de proteção ASR no cofre dos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c95ab-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="c95ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c95ab-104">SYNTAX</span></span>

### <span data-ttu-id="c95ab-105">ByFabricObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c95ab-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c95ab-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c95ab-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c95ab-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c95ab-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c95ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c95ab-108">DESCRIPTION</span></span>
<span data-ttu-id="c95ab-109">O cmdlet **Get-AzRecoveryServicesAsrProtectionContainer** Obtém contêineres de proteção do Azure site Recovery no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c95ab-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="c95ab-110">Um contêiner de proteção é um contêiner lógico para objetos protegidos (detectados) e protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c95ab-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="c95ab-111">As políticas de replicação definem as configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a um item de proteção.</span><span class="sxs-lookup"><span data-stu-id="c95ab-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="c95ab-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c95ab-112">EXAMPLES</span></span>

### <span data-ttu-id="c95ab-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c95ab-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="c95ab-114">Lista de contêiner de proteção no Fabric $fabric.</span><span class="sxs-lookup"><span data-stu-id="c95ab-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="c95ab-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c95ab-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c95ab-116">Contêiner de proteção no Fabric $fabric com nome.</span><span class="sxs-lookup"><span data-stu-id="c95ab-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="c95ab-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c95ab-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c95ab-118">Contêiner de proteção no Fabric $fabric com nome amigável.</span><span class="sxs-lookup"><span data-stu-id="c95ab-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="c95ab-119">OS</span><span class="sxs-lookup"><span data-stu-id="c95ab-119">PARAMETERS</span></span>

### <span data-ttu-id="c95ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95ab-120">-DefaultProfile</span></span>
<span data-ttu-id="c95ab-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c95ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c95ab-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="c95ab-122">-Fabric</span></span>
<span data-ttu-id="c95ab-123">Procure o contêiner de proteção na malha ASR especificada.</span><span class="sxs-lookup"><span data-stu-id="c95ab-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c95ab-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c95ab-124">-FriendlyName</span></span>
<span data-ttu-id="c95ab-125">Especifica o nome amigável do contêiner de proteção ASR a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="c95ab-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c95ab-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c95ab-126">-Name</span></span>
<span data-ttu-id="c95ab-127">Especifica o nome do contêiner de proteção ASR a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="c95ab-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c95ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95ab-128">CommonParameters</span></span>
<span data-ttu-id="c95ab-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c95ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95ab-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c95ab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95ab-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c95ab-131">INPUTS</span></span>

### <span data-ttu-id="c95ab-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c95ab-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c95ab-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c95ab-133">OUTPUTS</span></span>

### <span data-ttu-id="c95ab-134">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c95ab-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c95ab-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c95ab-135">NOTES</span></span>

## <span data-ttu-id="c95ab-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c95ab-136">RELATED LINKS</span></span>
