---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a25375a565db8d2c69a423aa95033033de3f0f8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599737"
---
# <span data-ttu-id="15d15-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="15d15-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="15d15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15d15-102">SYNOPSIS</span></span>
<span data-ttu-id="15d15-103">Obtém políticas de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="15d15-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="15d15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15d15-104">SYNTAX</span></span>

### <span data-ttu-id="15d15-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="15d15-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d15-106">ByName</span><span class="sxs-lookup"><span data-stu-id="15d15-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d15-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="15d15-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15d15-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15d15-108">DESCRIPTION</span></span>
<span data-ttu-id="15d15-109">O cmdlet **Get-AzRecoveryServicesAsrPolicy** Obtém a lista de políticas de replicação do Azure site Recovery configuradas ou uma política de replicação específica por nome.</span><span class="sxs-lookup"><span data-stu-id="15d15-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="15d15-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15d15-110">EXAMPLES</span></span>

### <span data-ttu-id="15d15-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15d15-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="15d15-112">Retuns a lista de políticas de replicação</span><span class="sxs-lookup"><span data-stu-id="15d15-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="15d15-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="15d15-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="15d15-114">Retuns a política de replicação com o nome.</span><span class="sxs-lookup"><span data-stu-id="15d15-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="15d15-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="15d15-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="15d15-116">Retorna a política de replicação com o nome amigável especificado.</span><span class="sxs-lookup"><span data-stu-id="15d15-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="15d15-117">OS</span><span class="sxs-lookup"><span data-stu-id="15d15-117">PARAMETERS</span></span>

### <span data-ttu-id="15d15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d15-118">-DefaultProfile</span></span>
<span data-ttu-id="15d15-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15d15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="15d15-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15d15-120">-FriendlyName</span></span>
<span data-ttu-id="15d15-121">Especifica o nome amigável da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="15d15-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="15d15-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="15d15-122">-Name</span></span>
<span data-ttu-id="15d15-123">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="15d15-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="15d15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d15-124">CommonParameters</span></span>
<span data-ttu-id="15d15-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15d15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d15-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d15-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d15-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15d15-127">INPUTS</span></span>

### <span data-ttu-id="15d15-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="15d15-128">None</span></span>

## <span data-ttu-id="15d15-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15d15-129">OUTPUTS</span></span>

### <span data-ttu-id="15d15-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="15d15-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="15d15-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15d15-131">NOTES</span></span>

## <span data-ttu-id="15d15-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15d15-132">RELATED LINKS</span></span>

[<span data-ttu-id="15d15-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="15d15-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="15d15-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="15d15-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
