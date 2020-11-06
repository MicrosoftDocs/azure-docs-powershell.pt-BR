---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602685"
---
# <span data-ttu-id="224cf-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="224cf-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="224cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="224cf-102">SYNOPSIS</span></span>
<span data-ttu-id="224cf-103">Obtém informações sobre máquinas virtuais gerenciadas por site Recovery.</span><span class="sxs-lookup"><span data-stu-id="224cf-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="224cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="224cf-104">SYNTAX</span></span>

### <span data-ttu-id="224cf-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="224cf-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224cf-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="224cf-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224cf-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="224cf-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="224cf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="224cf-108">DESCRIPTION</span></span>
<span data-ttu-id="224cf-109">O cmdlet **Get-AzureRmSiteRecoveryVM** Obtém informações sobre máquinas virtuais gerenciadas no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="224cf-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="224cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="224cf-110">EXAMPLES</span></span>

## <span data-ttu-id="224cf-111">OS</span><span class="sxs-lookup"><span data-stu-id="224cf-111">PARAMETERS</span></span>

### <span data-ttu-id="224cf-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="224cf-112">-FriendlyName</span></span>
<span data-ttu-id="224cf-113">Especifica o nome amigável da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="224cf-113">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="224cf-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="224cf-114">-Name</span></span>
<span data-ttu-id="224cf-115">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="224cf-115">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="224cf-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="224cf-116">-ProtectionContainer</span></span>
<span data-ttu-id="224cf-117">Especifica o objeto contêiner da proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="224cf-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="224cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224cf-118">-DefaultProfile</span></span>
<span data-ttu-id="224cf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="224cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="224cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224cf-120">CommonParameters</span></span>
<span data-ttu-id="224cf-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="224cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224cf-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224cf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224cf-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="224cf-123">INPUTS</span></span>

### <span data-ttu-id="224cf-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="224cf-124">ASRProtectionContainer</span></span>
<span data-ttu-id="224cf-125">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="224cf-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="224cf-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="224cf-126">ASRProtectionContainer</span></span>
<span data-ttu-id="224cf-127">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="224cf-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="224cf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="224cf-128">OUTPUTS</span></span>

### <span data-ttu-id="224cf-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="224cf-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="224cf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="224cf-130">NOTES</span></span>

## <span data-ttu-id="224cf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="224cf-131">RELATED LINKS</span></span>

[<span data-ttu-id="224cf-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="224cf-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
