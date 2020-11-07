---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773030"
---
# <span data-ttu-id="9252b-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9252b-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9252b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9252b-102">SYNOPSIS</span></span>
<span data-ttu-id="9252b-103">Obtém as propriedades de itens protegidos de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9252b-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="9252b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9252b-104">SYNTAX</span></span>

### <span data-ttu-id="9252b-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="9252b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9252b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9252b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9252b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9252b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9252b-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="9252b-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9252b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9252b-109">DESCRIPTION</span></span>
<span data-ttu-id="9252b-110">O cmdlet **Get-AzRecoveryServicesAsrReplicationProtectedItem** Obtém as propriedades de todos ou o item protegido de replicação ASR especificado do contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="9252b-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="9252b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9252b-111">EXAMPLES</span></span>

### <span data-ttu-id="9252b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9252b-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="9252b-113">Lista todos os itens protegidos de replicação no contêiner de proteção ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="9252b-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="9252b-114">OS</span><span class="sxs-lookup"><span data-stu-id="9252b-114">PARAMETERS</span></span>

### <span data-ttu-id="9252b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9252b-115">-DefaultProfile</span></span>
<span data-ttu-id="9252b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9252b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9252b-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9252b-117">-FriendlyName</span></span>
<span data-ttu-id="9252b-118">Especifica o nome amigável do item protegido de replicação a obter.</span><span class="sxs-lookup"><span data-stu-id="9252b-118">Specifies the friendly name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="9252b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9252b-119">-Name</span></span>
<span data-ttu-id="9252b-120">Especifica o nome do item protegido da replicação a obter.</span><span class="sxs-lookup"><span data-stu-id="9252b-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="9252b-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9252b-121">-ProtectableItem</span></span>
<span data-ttu-id="9252b-122">Especifica um objeto de item de proteção ASR.</span><span class="sxs-lookup"><span data-stu-id="9252b-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="9252b-123">O cmdlet obtém o item protegido de replicação ASR correspondente ao item protegido ASR especificado, se o item estiver protegido.</span><span class="sxs-lookup"><span data-stu-id="9252b-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9252b-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9252b-124">-ProtectionContainer</span></span>
<span data-ttu-id="9252b-125">Especifica o objeto de contêiner de proteção ASR do contêiner de proteção ASR correspondente ao item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="9252b-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9252b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9252b-126">CommonParameters</span></span>
<span data-ttu-id="9252b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9252b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9252b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9252b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9252b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9252b-129">INPUTS</span></span>

### <span data-ttu-id="9252b-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9252b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="9252b-131">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9252b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="9252b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9252b-132">OUTPUTS</span></span>

### <span data-ttu-id="9252b-133">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9252b-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9252b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9252b-134">NOTES</span></span>

## <span data-ttu-id="9252b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9252b-135">RELATED LINKS</span></span>

[<span data-ttu-id="9252b-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9252b-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9252b-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9252b-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9252b-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9252b-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
