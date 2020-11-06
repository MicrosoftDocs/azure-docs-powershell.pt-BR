---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431915"
---
# <span data-ttu-id="91e35-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e35-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="91e35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91e35-102">SYNOPSIS</span></span>
<span data-ttu-id="91e35-103">Obtém políticas de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="91e35-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91e35-104">SYNTAX</span></span>

### <span data-ttu-id="91e35-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="91e35-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e35-106">ByName</span><span class="sxs-lookup"><span data-stu-id="91e35-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91e35-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="91e35-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91e35-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91e35-108">DESCRIPTION</span></span>
<span data-ttu-id="91e35-109">O cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** Obtém a lista de políticas de replicação do Azure site Recovery configuradas ou uma política de replicação específica por nome.</span><span class="sxs-lookup"><span data-stu-id="91e35-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="91e35-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91e35-110">EXAMPLES</span></span>

### <span data-ttu-id="91e35-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91e35-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="91e35-112">Retuns a lista de políticas de replicação</span><span class="sxs-lookup"><span data-stu-id="91e35-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="91e35-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="91e35-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="91e35-114">Retuns a política de replicação com o nome.</span><span class="sxs-lookup"><span data-stu-id="91e35-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="91e35-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="91e35-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="91e35-116">Retorna a política de replicação com o nome amigável especificado.</span><span class="sxs-lookup"><span data-stu-id="91e35-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="91e35-117">OS</span><span class="sxs-lookup"><span data-stu-id="91e35-117">PARAMETERS</span></span>

### <span data-ttu-id="91e35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e35-118">-DefaultProfile</span></span>
<span data-ttu-id="91e35-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91e35-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91e35-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="91e35-120">-FriendlyName</span></span>
<span data-ttu-id="91e35-121">Especifica o nome amigável da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="91e35-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="91e35-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="91e35-122">-Name</span></span>
<span data-ttu-id="91e35-123">Especifica o nome da política de replicação ASR.</span><span class="sxs-lookup"><span data-stu-id="91e35-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="91e35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e35-124">CommonParameters</span></span>
<span data-ttu-id="91e35-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e35-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e35-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e35-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91e35-127">INPUTS</span></span>

### <span data-ttu-id="91e35-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="91e35-128">None</span></span>

## <span data-ttu-id="91e35-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91e35-129">OUTPUTS</span></span>

### <span data-ttu-id="91e35-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="91e35-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="91e35-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91e35-131">NOTES</span></span>

## <span data-ttu-id="91e35-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91e35-132">RELATED LINKS</span></span>

[<span data-ttu-id="91e35-133">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e35-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="91e35-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="91e35-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
