---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432891"
---
# <span data-ttu-id="e2404-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e2404-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="e2404-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2404-102">SYNOPSIS</span></span>
<span data-ttu-id="e2404-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e2404-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2404-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2404-104">SYNTAX</span></span>

### <span data-ttu-id="e2404-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2404-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2404-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="e2404-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2404-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e2404-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2404-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e2404-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2404-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e2404-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2404-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e2404-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2404-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2404-111">DESCRIPTION</span></span>
<span data-ttu-id="e2404-112">O cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e2404-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="e2404-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2404-113">EXAMPLES</span></span>

## <span data-ttu-id="e2404-114">OS</span><span class="sxs-lookup"><span data-stu-id="e2404-114">PARAMETERS</span></span>

### <span data-ttu-id="e2404-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e2404-115">-AddProtectedEntities</span></span>
<span data-ttu-id="e2404-116">Especifica uma matriz de entidades protegidas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="e2404-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e2404-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-118">-Append</span><span class="sxs-lookup"><span data-stu-id="e2404-118">-AppendGroup</span></span>
<span data-ttu-id="e2404-119">Indica que essa operação acrescenta o grupo ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e2404-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2404-120">-DefaultProfile</span></span>
<span data-ttu-id="e2404-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2404-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2404-122">-Grupo</span><span class="sxs-lookup"><span data-stu-id="e2404-122">-Group</span></span>
<span data-ttu-id="e2404-123">Especifica um grupo de plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e2404-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e2404-124">-RecoveryPlan</span></span>
<span data-ttu-id="e2404-125">Especifica um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e2404-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-126">-Remover o</span><span class="sxs-lookup"><span data-stu-id="e2404-126">-RemoveGroup</span></span>
<span data-ttu-id="e2404-127">Remove o grupo de plano de recuperação de recuperação de site especificado.</span><span class="sxs-lookup"><span data-stu-id="e2404-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="e2404-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="e2404-129">Especifica uma matriz de entidades protegidas.</span><span class="sxs-lookup"><span data-stu-id="e2404-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="e2404-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2404-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2404-131">CommonParameters</span></span>
<span data-ttu-id="e2404-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2404-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2404-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2404-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2404-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2404-134">INPUTS</span></span>

### <span data-ttu-id="e2404-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e2404-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="e2404-136">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e2404-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="e2404-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2404-137">OUTPUTS</span></span>

## <span data-ttu-id="e2404-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2404-138">NOTES</span></span>

## <span data-ttu-id="e2404-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2404-139">RELATED LINKS</span></span>

[<span data-ttu-id="e2404-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e2404-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e2404-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e2404-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
