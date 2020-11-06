---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609922"
---
# <span data-ttu-id="6848f-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6848f-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="6848f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6848f-102">SYNOPSIS</span></span>
<span data-ttu-id="6848f-103">Obtém as propriedades dos itens protegidos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6848f-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6848f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6848f-104">SYNTAX</span></span>

### <span data-ttu-id="6848f-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="6848f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6848f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6848f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6848f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6848f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6848f-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="6848f-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6848f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6848f-109">DESCRIPTION</span></span>
<span data-ttu-id="6848f-110">O cmdlet **Get-AzureRmSiteRecoveryReplicationProtectedItem** Obtém as propriedades dos itens protegidos do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6848f-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="6848f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6848f-111">EXAMPLES</span></span>

## <span data-ttu-id="6848f-112">OS</span><span class="sxs-lookup"><span data-stu-id="6848f-112">PARAMETERS</span></span>

### <span data-ttu-id="6848f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6848f-113">-DefaultProfile</span></span>
<span data-ttu-id="6848f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6848f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6848f-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6848f-115">-FriendlyName</span></span>
<span data-ttu-id="6848f-116">Especifica o nome amigável do item protegido de replicação que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6848f-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6848f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6848f-117">-Name</span></span>
<span data-ttu-id="6848f-118">Especifica o nome do item protegido de replicação que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6848f-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6848f-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6848f-119">-ProtectableItem</span></span>
<span data-ttu-id="6848f-120">Especifica o item que deve ser protegido correspondente ao item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="6848f-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6848f-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6848f-121">-ProtectionContainer</span></span>
<span data-ttu-id="6848f-122">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6848f-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6848f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6848f-123">CommonParameters</span></span>
<span data-ttu-id="6848f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6848f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6848f-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6848f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6848f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6848f-126">INPUTS</span></span>

### <span data-ttu-id="6848f-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6848f-127">ASRProtectableItem</span></span>
<span data-ttu-id="6848f-128">O parâmetro ' ProtectableItem ' aceita o valor do tipo ' ASRProtectableItem ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6848f-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="6848f-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6848f-129">ASRProtectionContainer</span></span>
<span data-ttu-id="6848f-130">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6848f-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="6848f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6848f-131">OUTPUTS</span></span>

### <span data-ttu-id="6848f-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6848f-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6848f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6848f-133">NOTES</span></span>

## <span data-ttu-id="6848f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6848f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6848f-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6848f-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6848f-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6848f-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="6848f-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6848f-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
