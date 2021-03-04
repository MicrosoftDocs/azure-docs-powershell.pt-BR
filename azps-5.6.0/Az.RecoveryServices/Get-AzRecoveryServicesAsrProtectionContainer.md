---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890594"
---
# <span data-ttu-id="d5b58-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5b58-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d5b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5b58-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b58-103">Obtém contêineres de proteção ASR no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d5b58-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="d5b58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d5b58-104">SYNTAX</span></span>

### <span data-ttu-id="d5b58-105">ByFabricObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d5b58-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b58-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d5b58-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5b58-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5b58-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5b58-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d5b58-108">DESCRIPTION</span></span>
<span data-ttu-id="d5b58-109">O cmdlet **Get-AzRecoveryServicesAsrProtectionContainer** obtém contêineres de proteção de Recuperação de Site do Azure no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d5b58-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="d5b58-110">Um contêiner de proteção é um contêiner lógico para objetos protegidos(descobertos) e protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="d5b58-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="d5b58-111">As políticas de replicação definem configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a um item protegido.</span><span class="sxs-lookup"><span data-stu-id="d5b58-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="d5b58-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5b58-112">EXAMPLES</span></span>

### <span data-ttu-id="d5b58-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5b58-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="d5b58-114">Lista de contêiner de proteção no $fabric.</span><span class="sxs-lookup"><span data-stu-id="d5b58-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="d5b58-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d5b58-115">Example 2</span></span>
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

<span data-ttu-id="d5b58-116">Contêiner de proteção em malha $fabric com nome.</span><span class="sxs-lookup"><span data-stu-id="d5b58-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="d5b58-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d5b58-117">Example 3</span></span>
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

<span data-ttu-id="d5b58-118">Contêiner de proteção em malha $fabric com Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="d5b58-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="d5b58-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d5b58-119">PARAMETERS</span></span>

### <span data-ttu-id="d5b58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b58-120">-DefaultProfile</span></span>
<span data-ttu-id="d5b58-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b58-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d5b58-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="d5b58-122">-Fabric</span></span>
<span data-ttu-id="d5b58-123">Procure o contêiner de proteção no tecido ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="d5b58-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="d5b58-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d5b58-124">-FriendlyName</span></span>
<span data-ttu-id="d5b58-125">Especifica o nome amigável do contêiner de proteção ASR a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="d5b58-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="d5b58-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d5b58-126">-Name</span></span>
<span data-ttu-id="d5b58-127">Especifica o nome do contêiner de proteção ASR a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="d5b58-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="d5b58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b58-128">CommonParameters</span></span>
<span data-ttu-id="d5b58-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b58-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5b58-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b58-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5b58-131">INPUTS</span></span>

### <span data-ttu-id="d5b58-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d5b58-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d5b58-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d5b58-133">OUTPUTS</span></span>

### <span data-ttu-id="d5b58-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5b58-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d5b58-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d5b58-135">NOTES</span></span>

## <span data-ttu-id="d5b58-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5b58-136">RELATED LINKS</span></span>
