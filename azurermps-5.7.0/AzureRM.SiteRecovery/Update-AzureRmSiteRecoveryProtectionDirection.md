---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: f7d8efcde5f60ed9cf6eb3aff7f86c9ea3171ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426585"
---
# <span data-ttu-id="c22e7-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c22e7-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="c22e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c22e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c22e7-103">Atualiza o servidor de origem e de destino para a proteção de um objeto de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="c22e7-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c22e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c22e7-104">SYNTAX</span></span>

### <span data-ttu-id="c22e7-105">ByPEObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c22e7-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c22e7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c22e7-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c22e7-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="c22e7-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22e7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c22e7-108">DESCRIPTION</span></span>
<span data-ttu-id="c22e7-109">O cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** atualiza o servidor de origem e de destino para a proteção de um objeto do Azure site Recovery após a conclusão de uma operação de failover de confirmação.</span><span class="sxs-lookup"><span data-stu-id="c22e7-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="c22e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c22e7-110">EXAMPLES</span></span>

## <span data-ttu-id="c22e7-111">OS</span><span class="sxs-lookup"><span data-stu-id="c22e7-111">PARAMETERS</span></span>

### <span data-ttu-id="c22e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22e7-112">-DefaultProfile</span></span>
<span data-ttu-id="c22e7-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c22e7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e7-114">-Direction</span><span class="sxs-lookup"><span data-stu-id="c22e7-114">-Direction</span></span>
<span data-ttu-id="c22e7-115">Especifica a direção da confirmação.</span><span class="sxs-lookup"><span data-stu-id="c22e7-115">Specifies the direction of the commit.</span></span>
<span data-ttu-id="c22e7-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c22e7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c22e7-117">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c22e7-117">PrimaryToRecovery</span></span>
- <span data-ttu-id="c22e7-118">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c22e7-118">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e7-119">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c22e7-119">-ProtectionEntity</span></span>
<span data-ttu-id="c22e7-120">Especifica o objeto da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="c22e7-120">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e7-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c22e7-121">-RecoveryPlan</span></span>
<span data-ttu-id="c22e7-122">Especifica um objeto de plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c22e7-122">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e7-123">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c22e7-123">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22e7-124">CommonParameters</span></span>
<span data-ttu-id="c22e7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22e7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22e7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c22e7-127">INPUTS</span></span>

### <span data-ttu-id="c22e7-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c22e7-128">ASRProtectionEntity</span></span>
<span data-ttu-id="c22e7-129">O parâmetro ' ProtectionEntity ' aceita o valor do tipo ' ASRProtectionEntity ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c22e7-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="c22e7-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c22e7-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="c22e7-131">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c22e7-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="c22e7-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c22e7-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c22e7-133">O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c22e7-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c22e7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c22e7-134">OUTPUTS</span></span>

### <span data-ttu-id="c22e7-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c22e7-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c22e7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c22e7-136">NOTES</span></span>

## <span data-ttu-id="c22e7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c22e7-137">RELATED LINKS</span></span>

