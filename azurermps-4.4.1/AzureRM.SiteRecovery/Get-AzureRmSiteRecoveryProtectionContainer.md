---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440551"
---
# <span data-ttu-id="93f50-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="93f50-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="93f50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93f50-102">SYNOPSIS</span></span>
<span data-ttu-id="93f50-103">Obtém contêineres de proteção para o cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="93f50-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93f50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93f50-104">SYNTAX</span></span>

### <span data-ttu-id="93f50-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="93f50-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f50-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="93f50-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f50-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="93f50-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93f50-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="93f50-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f50-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="93f50-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93f50-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="93f50-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93f50-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93f50-111">DESCRIPTION</span></span>
<span data-ttu-id="93f50-112">O cmdlet **Get-AzureRmSiteRecoveryProtectionContainer** Obtém contêineres de proteção para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="93f50-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="93f50-113">Um contêiner de proteção é um contêiner lógico para objetos protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="93f50-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="93f50-114">As políticas de proteção definem as configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a uma entidade protegida.</span><span class="sxs-lookup"><span data-stu-id="93f50-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="93f50-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93f50-115">EXAMPLES</span></span>

## <span data-ttu-id="93f50-116">OS</span><span class="sxs-lookup"><span data-stu-id="93f50-116">PARAMETERS</span></span>

### <span data-ttu-id="93f50-117">-Fabric</span><span class="sxs-lookup"><span data-stu-id="93f50-117">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f50-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="93f50-118">-FriendlyName</span></span>
<span data-ttu-id="93f50-119">Especifica o nome amigável do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="93f50-119">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f50-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="93f50-120">-Name</span></span>
<span data-ttu-id="93f50-121">Especifica o nome do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="93f50-121">Specifies the name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f50-122">-DefaultProfile</span></span>
<span data-ttu-id="93f50-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93f50-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93f50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f50-124">CommonParameters</span></span>
<span data-ttu-id="93f50-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f50-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f50-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f50-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93f50-127">INPUTS</span></span>

### <span data-ttu-id="93f50-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="93f50-128">ASRFabric</span></span>
<span data-ttu-id="93f50-129">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="93f50-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="93f50-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93f50-130">OUTPUTS</span></span>

### <span data-ttu-id="93f50-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="93f50-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="93f50-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93f50-132">NOTES</span></span>

## <span data-ttu-id="93f50-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93f50-133">RELATED LINKS</span></span>

