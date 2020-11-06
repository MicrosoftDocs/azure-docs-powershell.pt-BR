---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429056"
---
# <span data-ttu-id="7878b-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="7878b-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="7878b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7878b-102">SYNOPSIS</span></span>
<span data-ttu-id="7878b-103">Atualiza o servidor de origem e de destino para a proteção de um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="7878b-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7878b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7878b-104">SYNTAX</span></span>

### <span data-ttu-id="7878b-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="7878b-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7878b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7878b-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7878b-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="7878b-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7878b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7878b-108">DESCRIPTION</span></span>
<span data-ttu-id="7878b-109">O cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** atualiza o servidor de origem e de destino para a proteção de um objeto do Azure site Recovery após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="7878b-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="7878b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7878b-110">EXAMPLES</span></span>

## <span data-ttu-id="7878b-111">OS</span><span class="sxs-lookup"><span data-stu-id="7878b-111">PARAMETERS</span></span>

### <span data-ttu-id="7878b-112">-Direction</span><span class="sxs-lookup"><span data-stu-id="7878b-112">-Direction</span></span>
<span data-ttu-id="7878b-113">Especifica a direção da confirmação.</span><span class="sxs-lookup"><span data-stu-id="7878b-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="7878b-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7878b-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7878b-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7878b-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="7878b-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7878b-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7878b-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7878b-117">-ProtectionEntity</span></span>
<span data-ttu-id="7878b-118">Especifica o objeto da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="7878b-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7878b-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7878b-119">-RecoveryPlan</span></span>
<span data-ttu-id="7878b-120">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7878b-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7878b-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7878b-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7878b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7878b-122">-DefaultProfile</span></span>
<span data-ttu-id="7878b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7878b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7878b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7878b-124">CommonParameters</span></span>
<span data-ttu-id="7878b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7878b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7878b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7878b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7878b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7878b-127">INPUTS</span></span>

### <span data-ttu-id="7878b-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7878b-128">ASRProtectionEntity</span></span>
<span data-ttu-id="7878b-129">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7878b-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="7878b-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7878b-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="7878b-131">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7878b-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="7878b-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7878b-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7878b-133">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7878b-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7878b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7878b-134">OUTPUTS</span></span>

### <span data-ttu-id="7878b-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7878b-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7878b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7878b-136">NOTES</span></span>

## <span data-ttu-id="7878b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7878b-137">RELATED LINKS</span></span>

