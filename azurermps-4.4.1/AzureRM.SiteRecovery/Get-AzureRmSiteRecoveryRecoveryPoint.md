---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 68e005a4e54277ad1be304911645c3eeda455d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610711"
---
# <span data-ttu-id="a40d4-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a40d4-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="a40d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a40d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a40d4-103">Obtém pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="a40d4-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a40d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a40d4-104">SYNTAX</span></span>

### <span data-ttu-id="a40d4-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="a40d4-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40d4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a40d4-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a40d4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a40d4-107">DESCRIPTION</span></span>
<span data-ttu-id="a40d4-108">O cmdlet **Get-AzureRmSiteRecoveryRecoveryPoint** Obtém a lista de pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="a40d4-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="a40d4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a40d4-109">EXAMPLES</span></span>

## <span data-ttu-id="a40d4-110">OS</span><span class="sxs-lookup"><span data-stu-id="a40d4-110">PARAMETERS</span></span>

### <span data-ttu-id="a40d4-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="a40d4-111">-Name</span></span>
<span data-ttu-id="a40d4-112">Especifica o nome do ponto de recuperação que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a40d4-112">Specifies the name of the recovery point this cmdlet gets.</span></span>

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

### <span data-ttu-id="a40d4-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a40d4-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a40d4-114">Especifica o objeto de item protegido da replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a40d4-114">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a40d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40d4-115">-DefaultProfile</span></span>
<span data-ttu-id="a40d4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a40d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40d4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40d4-117">CommonParameters</span></span>
<span data-ttu-id="a40d4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40d4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40d4-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40d4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40d4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a40d4-120">INPUTS</span></span>

### <span data-ttu-id="a40d4-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a40d4-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="a40d4-122">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a40d4-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="a40d4-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a40d4-123">OUTPUTS</span></span>

### <span data-ttu-id="a40d4-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a40d4-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a40d4-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a40d4-125">NOTES</span></span>

## <span data-ttu-id="a40d4-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a40d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="a40d4-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a40d4-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a40d4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a40d4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a40d4-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a40d4-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a40d4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a40d4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a40d4-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a40d4-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
