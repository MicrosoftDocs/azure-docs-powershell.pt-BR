---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440944"
---
# <span data-ttu-id="02319-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="02319-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="02319-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02319-102">SYNOPSIS</span></span>
<span data-ttu-id="02319-103">Obtém uma lista de entidades protegidas ou protegidas no cofre de recuperação do site atual.</span><span class="sxs-lookup"><span data-stu-id="02319-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02319-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02319-104">SYNTAX</span></span>

### <span data-ttu-id="02319-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="02319-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02319-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="02319-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02319-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="02319-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02319-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02319-108">DESCRIPTION</span></span>
<span data-ttu-id="02319-109">O cmdlet **Get-AzureRmSiteRecoveryProtectionEntity** Obtém uma lista de entidades protegidas ou protegidas, como máquinas virtuais, no cofre atual do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="02319-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="02319-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02319-110">EXAMPLES</span></span>

## <span data-ttu-id="02319-111">OS</span><span class="sxs-lookup"><span data-stu-id="02319-111">PARAMETERS</span></span>

### <span data-ttu-id="02319-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="02319-112">-FriendlyName</span></span>
<span data-ttu-id="02319-113">Especifica o nome amigável da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="02319-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="02319-114">-Name</span></span>
<span data-ttu-id="02319-115">Especifica o nome da entidade de proteção.</span><span class="sxs-lookup"><span data-stu-id="02319-115">Specifies the name of the protection entity.</span></span>

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

### <span data-ttu-id="02319-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="02319-116">-ProtectionContainer</span></span>
<span data-ttu-id="02319-117">Especifica o objeto do contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="02319-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02319-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02319-118">-DefaultProfile</span></span>
<span data-ttu-id="02319-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02319-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02319-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02319-120">CommonParameters</span></span>
<span data-ttu-id="02319-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02319-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02319-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02319-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02319-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02319-123">INPUTS</span></span>

### <span data-ttu-id="02319-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="02319-124">ASRProtectionContainer</span></span>
<span data-ttu-id="02319-125">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="02319-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="02319-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02319-126">OUTPUTS</span></span>

### <span data-ttu-id="02319-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="02319-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="02319-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02319-128">NOTES</span></span>

## <span data-ttu-id="02319-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02319-129">RELATED LINKS</span></span>

[<span data-ttu-id="02319-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="02319-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
