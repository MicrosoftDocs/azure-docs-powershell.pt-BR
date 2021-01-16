---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263306"
---
# <span data-ttu-id="d3471-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d3471-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="d3471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3471-102">SYNOPSIS</span></span>
<span data-ttu-id="d3471-103">Obtenha os itens protegidos em um contêiner de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="d3471-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="d3471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3471-104">SYNTAX</span></span>

### <span data-ttu-id="d3471-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3471-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3471-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d3471-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3471-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d3471-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3471-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3471-108">DESCRIPTION</span></span>
<span data-ttu-id="d3471-109">O cmdlet **Get-AzRecoveryServicesAsrProtectableItem** Obtém os itens que protegem em um contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d3471-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d3471-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3471-110">EXAMPLES</span></span>

### <span data-ttu-id="d3471-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3471-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="d3471-112">Obtém todos os itens que protegem no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="d3471-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="d3471-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d3471-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="d3471-114">Obtenha os itens protegidos no contêiner de proteção ASR especificado e com o nome amigável fornecido.</span><span class="sxs-lookup"><span data-stu-id="d3471-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="d3471-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d3471-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="d3471-116">Obtém todos os itens que protegem no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="d3471-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="d3471-117">OS</span><span class="sxs-lookup"><span data-stu-id="d3471-117">PARAMETERS</span></span>

### <span data-ttu-id="d3471-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3471-118">-DefaultProfile</span></span>
<span data-ttu-id="d3471-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3471-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d3471-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d3471-120">-FriendlyName</span></span>
<span data-ttu-id="d3471-121">Especifica o nome amigável do item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="d3471-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="d3471-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3471-122">-Name</span></span>
<span data-ttu-id="d3471-123">Especifica o nome do item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="d3471-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="d3471-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d3471-124">-ProtectionContainer</span></span>
<span data-ttu-id="d3471-125">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d3471-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d3471-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3471-126">CommonParameters</span></span>
<span data-ttu-id="d3471-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3471-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3471-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3471-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3471-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3471-129">INPUTS</span></span>

### <span data-ttu-id="d3471-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d3471-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d3471-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3471-131">OUTPUTS</span></span>

### <span data-ttu-id="d3471-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d3471-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d3471-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3471-133">NOTES</span></span>

## <span data-ttu-id="d3471-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3471-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3471-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d3471-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="d3471-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d3471-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
