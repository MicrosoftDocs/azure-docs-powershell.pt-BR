---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433394"
---
# <span data-ttu-id="75570-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="75570-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="75570-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75570-102">SYNOPSIS</span></span>
<span data-ttu-id="75570-103">Obtém informações sobre máquinas virtuais gerenciadas por site Recovery.</span><span class="sxs-lookup"><span data-stu-id="75570-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75570-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75570-104">SYNTAX</span></span>

### <span data-ttu-id="75570-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="75570-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75570-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="75570-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75570-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="75570-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75570-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75570-108">DESCRIPTION</span></span>
<span data-ttu-id="75570-109">O cmdlet **Get-AzureRmSiteRecoveryVM** Obtém informações sobre máquinas virtuais gerenciadas no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="75570-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="75570-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75570-110">EXAMPLES</span></span>

## <span data-ttu-id="75570-111">OS</span><span class="sxs-lookup"><span data-stu-id="75570-111">PARAMETERS</span></span>

### <span data-ttu-id="75570-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75570-112">-DefaultProfile</span></span>
<span data-ttu-id="75570-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75570-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75570-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="75570-114">-FriendlyName</span></span>
<span data-ttu-id="75570-115">Especifica o nome amigável da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75570-115">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="75570-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="75570-116">-Name</span></span>
<span data-ttu-id="75570-117">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75570-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="75570-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="75570-118">-ProtectionContainer</span></span>
<span data-ttu-id="75570-119">Especifica o objeto contêiner da proteção de recuperação de sites.</span><span class="sxs-lookup"><span data-stu-id="75570-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75570-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75570-120">CommonParameters</span></span>
<span data-ttu-id="75570-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75570-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75570-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75570-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75570-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75570-123">INPUTS</span></span>

### <span data-ttu-id="75570-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="75570-124">ASRProtectionContainer</span></span>
<span data-ttu-id="75570-125">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="75570-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="75570-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="75570-126">ASRProtectionContainer</span></span>
<span data-ttu-id="75570-127">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="75570-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="75570-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75570-128">OUTPUTS</span></span>

### <span data-ttu-id="75570-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="75570-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="75570-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75570-130">NOTES</span></span>

## <span data-ttu-id="75570-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75570-131">RELATED LINKS</span></span>

[<span data-ttu-id="75570-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="75570-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
