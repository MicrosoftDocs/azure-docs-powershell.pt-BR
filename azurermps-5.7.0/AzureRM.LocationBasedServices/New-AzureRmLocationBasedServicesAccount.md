---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428205"
---
# <span data-ttu-id="877d7-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="877d7-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="877d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="877d7-102">SYNOPSIS</span></span>
<span data-ttu-id="877d7-103">Cria uma conta de serviços com base em local.</span><span class="sxs-lookup"><span data-stu-id="877d7-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="877d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="877d7-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="877d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="877d7-105">DESCRIPTION</span></span>
<span data-ttu-id="877d7-106">O cmdlet **New-AzureRmLocationBasedServicesAccount** cria uma conta de serviços com base em local com a SKU especificada.</span><span class="sxs-lookup"><span data-stu-id="877d7-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="877d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="877d7-107">EXAMPLES</span></span>

### <span data-ttu-id="877d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="877d7-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="877d7-109">Cria uma nova conta de serviços com base em local chamada myaccount no grupo de recursos grupo de recursos com o SKU S0 e uma marca.</span><span class="sxs-lookup"><span data-stu-id="877d7-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="877d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="877d7-110">PARAMETERS</span></span>

### <span data-ttu-id="877d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877d7-111">-DefaultProfile</span></span>
<span data-ttu-id="877d7-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="877d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="877d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="877d7-113">-Force</span></span>
<span data-ttu-id="877d7-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="877d7-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="877d7-115">-Name</span></span>
<span data-ttu-id="877d7-116">Nome da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="877d7-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="877d7-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="877d7-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="877d7-119">-SkuName</span></span>
<span data-ttu-id="877d7-120">Nome SKU da conta de serviços baseados em local.</span><span class="sxs-lookup"><span data-stu-id="877d7-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="877d7-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="877d7-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="877d7-122">S0</span><span class="sxs-lookup"><span data-stu-id="877d7-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="877d7-123">-Tag</span></span>
<span data-ttu-id="877d7-124">Marcas de conta de serviços baseado em local.</span><span class="sxs-lookup"><span data-stu-id="877d7-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="877d7-125">-Confirm</span></span>
<span data-ttu-id="877d7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="877d7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="877d7-127">-WhatIf</span></span>
<span data-ttu-id="877d7-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="877d7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="877d7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="877d7-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877d7-130">CommonParameters</span></span>
<span data-ttu-id="877d7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877d7-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="877d7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877d7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="877d7-133">INPUTS</span></span>

### <span data-ttu-id="877d7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="877d7-134">System.String</span></span>

## <span data-ttu-id="877d7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="877d7-135">OUTPUTS</span></span>

### <span data-ttu-id="877d7-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="877d7-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="877d7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="877d7-137">NOTES</span></span>

<span data-ttu-id="877d7-138">A criação de uma conta de serviços com base em locais exige responder a um aviso para aceitar termos (consulte https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="877d7-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="877d7-139">O parâmetro-Force pode ser usado para indicar a aceitação dos termos.</span><span class="sxs-lookup"><span data-stu-id="877d7-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="877d7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="877d7-140">RELATED LINKS</span></span>
