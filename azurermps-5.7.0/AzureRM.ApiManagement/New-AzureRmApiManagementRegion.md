---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: dc51caee3a0cb8d5571a5a316c2018c30abbe239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441514"
---
# <span data-ttu-id="90c4d-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="90c4d-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="90c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="90c4d-103">Cria uma instância de PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="90c4d-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90c4d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90c4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="90c4d-106">Comando auxiliar para criar uma instância de PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="90c4d-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="90c4d-107">Esse comando deve ser usado com o comando New-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="90c4d-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="90c4d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90c4d-108">EXAMPLES</span></span>

### <span data-ttu-id="90c4d-109">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90c4d-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="90c4d-110">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="90c4d-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="90c4d-111">Cria um serviço ApiManagement de VpnType externo na região oeste dos EUA, com uma região adicional nos EUA.</span><span class="sxs-lookup"><span data-stu-id="90c4d-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="90c4d-112">OS</span><span class="sxs-lookup"><span data-stu-id="90c4d-112">PARAMETERS</span></span>

### <span data-ttu-id="90c4d-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="90c4d-113">-Capacity</span></span>
<span data-ttu-id="90c4d-114">Capacidade de SKU da região adicional do serviço de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="90c4d-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="90c4d-115">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="90c4d-115">Default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c4d-116">-DefaultProfile</span></span>
<span data-ttu-id="90c4d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90c4d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="90c4d-118">-Local</span><span class="sxs-lookup"><span data-stu-id="90c4d-118">-Location</span></span>
<span data-ttu-id="90c4d-119">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="90c4d-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="90c4d-120">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="90c4d-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c4d-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="90c4d-121">-VirtualNetwork</span></span>
<span data-ttu-id="90c4d-122">Configuração de rede virtual da região de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="90c4d-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="90c4d-123">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="90c4d-123">Default value is $null.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c4d-124">CommonParameters</span></span>
<span data-ttu-id="90c4d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c4d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c4d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c4d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90c4d-127">INPUTS</span></span>

### <span data-ttu-id="90c4d-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="90c4d-128">None</span></span>
<span data-ttu-id="90c4d-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="90c4d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90c4d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90c4d-130">OUTPUTS</span></span>

### <span data-ttu-id="90c4d-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="90c4d-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="90c4d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90c4d-132">NOTES</span></span>

## <span data-ttu-id="90c4d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90c4d-133">RELATED LINKS</span></span>

