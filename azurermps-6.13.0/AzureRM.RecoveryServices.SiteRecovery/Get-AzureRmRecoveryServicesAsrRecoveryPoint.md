---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428402"
---
# <span data-ttu-id="07d04-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="07d04-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="07d04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07d04-102">SYNOPSIS</span></span>
<span data-ttu-id="07d04-103">Obtém os pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="07d04-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07d04-104">SYNTAX</span></span>

### <span data-ttu-id="07d04-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="07d04-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d04-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="07d04-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07d04-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07d04-107">DESCRIPTION</span></span>
<span data-ttu-id="07d04-108">O cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPoint** Obtém a lista de pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="07d04-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="07d04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07d04-109">EXAMPLES</span></span>

### <span data-ttu-id="07d04-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07d04-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="07d04-111">Obtém pontos de recuperação para o item protegido de replicação ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="07d04-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="07d04-112">OS</span><span class="sxs-lookup"><span data-stu-id="07d04-112">PARAMETERS</span></span>

### <span data-ttu-id="07d04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d04-113">-DefaultProfile</span></span>
<span data-ttu-id="07d04-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07d04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="07d04-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="07d04-115">-Name</span></span>
<span data-ttu-id="07d04-116">Especifica o nome do ponto de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="07d04-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="07d04-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07d04-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="07d04-118">Especifica o objeto de item protegido da replicação do Azure site Recovery para o qual obter a lista de pontos de recuperação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="07d04-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07d04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d04-119">CommonParameters</span></span>
<span data-ttu-id="07d04-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d04-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d04-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07d04-122">INPUTS</span></span>

### <span data-ttu-id="07d04-123">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07d04-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="07d04-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07d04-124">OUTPUTS</span></span>

### <span data-ttu-id="07d04-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="07d04-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="07d04-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07d04-126">NOTES</span></span>

## <span data-ttu-id="07d04-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07d04-127">RELATED LINKS</span></span>

[<span data-ttu-id="07d04-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d04-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07d04-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d04-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07d04-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d04-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07d04-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d04-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="07d04-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d04-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
