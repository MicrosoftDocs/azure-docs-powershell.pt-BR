---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e9559993e122e5b713228630b3b783b1f0e6a981
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892382"
---
# <span data-ttu-id="96c4d-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="96c4d-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="96c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="96c4d-103">Obtém políticas de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="96c4d-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="96c4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96c4d-104">SYNTAX</span></span>

### <span data-ttu-id="96c4d-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96c4d-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c4d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="96c4d-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c4d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="96c4d-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96c4d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="96c4d-109">O cmdlet **Get-AzRecoveryServicesAsrPolicy** obtém a lista de políticas de replicação configuradas do Azure Site Recovery ou uma política de replicação específica por nome.</span><span class="sxs-lookup"><span data-stu-id="96c4d-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="96c4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96c4d-110">EXAMPLES</span></span>

### <span data-ttu-id="96c4d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96c4d-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="96c4d-112">Retorna a lista de políticas de replicação</span><span class="sxs-lookup"><span data-stu-id="96c4d-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="96c4d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="96c4d-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="96c4d-114">Retorna a política de replicação com nome.</span><span class="sxs-lookup"><span data-stu-id="96c4d-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="96c4d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="96c4d-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="96c4d-116">Retorna a política de replicação com o nome amigável especificado.</span><span class="sxs-lookup"><span data-stu-id="96c4d-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="96c4d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96c4d-117">PARAMETERS</span></span>

### <span data-ttu-id="96c4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c4d-118">-DefaultProfile</span></span>
<span data-ttu-id="96c4d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96c4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="96c4d-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="96c4d-120">-FriendlyName</span></span>
<span data-ttu-id="96c4d-121">Especifica o nome amigável da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="96c4d-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c4d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="96c4d-122">-Name</span></span>
<span data-ttu-id="96c4d-123">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="96c4d-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c4d-124">CommonParameters</span></span>
<span data-ttu-id="96c4d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c4d-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c4d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96c4d-127">INPUTS</span></span>

### <span data-ttu-id="96c4d-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="96c4d-128">None</span></span>

## <span data-ttu-id="96c4d-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96c4d-129">OUTPUTS</span></span>

### <span data-ttu-id="96c4d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="96c4d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="96c4d-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="96c4d-131">NOTES</span></span>

## <span data-ttu-id="96c4d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96c4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="96c4d-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="96c4d-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="96c4d-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="96c4d-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
