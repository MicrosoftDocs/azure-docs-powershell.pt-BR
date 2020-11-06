---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602403"
---
# <span data-ttu-id="7973d-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7973d-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="7973d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7973d-102">SYNOPSIS</span></span>
<span data-ttu-id="7973d-103">Edita um plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="7973d-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7973d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7973d-104">SYNTAX</span></span>

### <span data-ttu-id="7973d-105">Append (padrão)</span><span class="sxs-lookup"><span data-stu-id="7973d-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7973d-106">Remover o</span><span class="sxs-lookup"><span data-stu-id="7973d-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7973d-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7973d-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7973d-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7973d-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7973d-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7973d-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7973d-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7973d-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7973d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7973d-111">DESCRIPTION</span></span>
<span data-ttu-id="7973d-112">O cmdlet **Edit-AzureRmSiteRecoveryRecoveryPlan** edita um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7973d-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="7973d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7973d-113">EXAMPLES</span></span>

## <span data-ttu-id="7973d-114">OS</span><span class="sxs-lookup"><span data-stu-id="7973d-114">PARAMETERS</span></span>

### <span data-ttu-id="7973d-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7973d-115">-AddProtectedEntities</span></span>
<span data-ttu-id="7973d-116">Especifica uma matriz de entidades protegidas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="7973d-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7973d-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-118">-Append</span><span class="sxs-lookup"><span data-stu-id="7973d-118">-AppendGroup</span></span>
<span data-ttu-id="7973d-119">Indica que essa operação acrescenta o grupo ao objeto do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7973d-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-120">-Grupo</span><span class="sxs-lookup"><span data-stu-id="7973d-120">-Group</span></span>
<span data-ttu-id="7973d-121">Especifica um grupo de plano de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="7973d-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7973d-122">-RecoveryPlan</span></span>
<span data-ttu-id="7973d-123">Especifica um plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7973d-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-124">-Remover o</span><span class="sxs-lookup"><span data-stu-id="7973d-124">-RemoveGroup</span></span>
<span data-ttu-id="7973d-125">Remove o grupo de plano de recuperação de recuperação de site especificado.</span><span class="sxs-lookup"><span data-stu-id="7973d-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="7973d-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="7973d-127">Especifica uma matriz de entidades protegidas.</span><span class="sxs-lookup"><span data-stu-id="7973d-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="7973d-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7973d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7973d-129">-DefaultProfile</span></span>
<span data-ttu-id="7973d-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7973d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7973d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7973d-131">CommonParameters</span></span>
<span data-ttu-id="7973d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7973d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7973d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7973d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7973d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7973d-134">INPUTS</span></span>

### <span data-ttu-id="7973d-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7973d-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="7973d-136">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7973d-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="7973d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7973d-137">OUTPUTS</span></span>

## <span data-ttu-id="7973d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7973d-138">NOTES</span></span>

## <span data-ttu-id="7973d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7973d-139">RELATED LINKS</span></span>

[<span data-ttu-id="7973d-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7973d-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="7973d-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7973d-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
