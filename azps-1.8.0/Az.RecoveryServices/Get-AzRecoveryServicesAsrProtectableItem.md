---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 31dc0a5e7fb9bba20aea6fb6395ec59ba54d0e2c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399831"
---
# <span data-ttu-id="1a5e6-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1a5e6-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="1a5e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5e6-103">Obter os itens protegidos em um contêiner de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="1a5e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a5e6-104">SYNTAX</span></span>

### <span data-ttu-id="1a5e6-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1a5e6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a5e6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1a5e6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a5e6-107">ByObjectWithBjlyName</span><span class="sxs-lookup"><span data-stu-id="1a5e6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a5e6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a5e6-108">DESCRIPTION</span></span>
<span data-ttu-id="1a5e6-109">O cmdlet **Get-AzRecoveryServicesAsrProtectableItem** obtém os itens protegidos em um Contêiner de Proteção de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="1a5e6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a5e6-110">EXAMPLES</span></span>

### <span data-ttu-id="1a5e6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1a5e6-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="1a5e6-112">Obtém todos os itens protegidos no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="1a5e6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1a5e6-113">Example 2</span></span>
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

<span data-ttu-id="1a5e6-114">Obter os itens protegidos no contêiner de proteção ASR especificado e com um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="1a5e6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1a5e6-115">Example 3</span></span>
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

<span data-ttu-id="1a5e6-116">Obtém todos os itens protegidos no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="1a5e6-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a5e6-117">PARAMETERS</span></span>

### <span data-ttu-id="1a5e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5e6-118">-DefaultProfile</span></span>
<span data-ttu-id="1a5e6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1a5e6-120">-Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="1a5e6-120">-FriendlyName</span></span>
<span data-ttu-id="1a5e6-121">Especifica o nome amigável do item protegido pelo ASR.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="1a5e6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a5e6-122">-Name</span></span>
<span data-ttu-id="1a5e6-123">Especifica o nome do item protegido pelo ASR.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="1a5e6-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a5e6-124">-ProtectionContainer</span></span>
<span data-ttu-id="1a5e6-125">Especifica o objeto Contêiner de Proteção de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="1a5e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5e6-126">CommonParameters</span></span>
<span data-ttu-id="1a5e6-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5e6-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5e6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5e6-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-129">INPUTS</span></span>

### <span data-ttu-id="1a5e6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a5e6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="1a5e6-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-131">OUTPUTS</span></span>

### <span data-ttu-id="1a5e6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1a5e6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="1a5e6-133">Notas</span><span class="sxs-lookup"><span data-stu-id="1a5e6-133">NOTES</span></span>

## <span data-ttu-id="1a5e6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a5e6-134">RELATED LINKS</span></span>


