---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 13a6478f6124a6c7e017854918abfdf8b07165f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771410"
---
# <span data-ttu-id="eb212-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb212-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="eb212-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb212-102">SYNOPSIS</span></span>
<span data-ttu-id="eb212-103">Cria uma instância de PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="eb212-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="eb212-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb212-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb212-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb212-105">DESCRIPTION</span></span>
<span data-ttu-id="eb212-106">Comando auxiliar para criar uma instância de PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="eb212-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="eb212-107">Esse comando deve ser usado com o comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="eb212-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="eb212-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb212-108">EXAMPLES</span></span>

### <span data-ttu-id="eb212-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb212-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="eb212-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb212-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="eb212-111">Cria um serviço ApiManagement de VpnType externo na região oeste dos EUA, com uma região adicional nos EUA.</span><span class="sxs-lookup"><span data-stu-id="eb212-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="eb212-112">OS</span><span class="sxs-lookup"><span data-stu-id="eb212-112">PARAMETERS</span></span>

### <span data-ttu-id="eb212-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="eb212-113">-Capacity</span></span>
<span data-ttu-id="eb212-114">Capacidade de SKU da região adicional do serviço de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb212-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="eb212-115">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="eb212-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb212-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb212-116">-DefaultProfile</span></span>
<span data-ttu-id="eb212-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb212-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb212-118">-Local</span><span class="sxs-lookup"><span data-stu-id="eb212-118">-Location</span></span>
<span data-ttu-id="eb212-119">Especifica o local da nova região de implantação entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="eb212-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="eb212-120">Para obter locais válidos, use o cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="eb212-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb212-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb212-121">-VirtualNetwork</span></span>
<span data-ttu-id="eb212-122">Configuração de rede virtual da região de implantação de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb212-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="eb212-123">O valor padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="eb212-123">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb212-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb212-124">CommonParameters</span></span>
<span data-ttu-id="eb212-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb212-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb212-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb212-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb212-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb212-127">INPUTS</span></span>

### <span data-ttu-id="eb212-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb212-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="eb212-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb212-129">OUTPUTS</span></span>

### <span data-ttu-id="eb212-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb212-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="eb212-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb212-131">NOTES</span></span>

## <span data-ttu-id="eb212-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb212-132">RELATED LINKS</span></span>
