---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441512"
---
# <span data-ttu-id="e4eea-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4eea-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="e4eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4eea-102">SYNOPSIS</span></span>
<span data-ttu-id="e4eea-103">Cria uma instância de PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="e4eea-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4eea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4eea-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4eea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4eea-105">DESCRIPTION</span></span>
<span data-ttu-id="e4eea-106">O cmdlet **New-AzureRmApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="e4eea-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="e4eea-107">Esse comando é usado com o cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="e4eea-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="e4eea-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4eea-108">EXAMPLES</span></span>

### <span data-ttu-id="e4eea-109">Exemplo 1: criar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="e4eea-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="e4eea-110">Este exemplo cria uma rede virtual e, em seguida, chama o cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="e4eea-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="e4eea-111">OS</span><span class="sxs-lookup"><span data-stu-id="e4eea-111">PARAMETERS</span></span>

### <span data-ttu-id="e4eea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4eea-112">-DefaultProfile</span></span>
<span data-ttu-id="e4eea-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4eea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e4eea-114">-Local</span><span class="sxs-lookup"><span data-stu-id="e4eea-114">-Location</span></span>
<span data-ttu-id="e4eea-115">Especifica o local entre a região com suporte para o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e4eea-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="e4eea-116">Para obter locais válidos, use o cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | em que {$ _. ResourceTypes [0]. ResourceTypename-EQ "serviço"} | Locais do Select-Object</span><span class="sxs-lookup"><span data-stu-id="e4eea-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="e4eea-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="e4eea-117">-SubnetResourceId</span></span>
<span data-ttu-id="e4eea-118">Especifica a ID do recurso de sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e4eea-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="e4eea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4eea-119">CommonParameters</span></span>
<span data-ttu-id="e4eea-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4eea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4eea-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4eea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4eea-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4eea-122">INPUTS</span></span>

### <span data-ttu-id="e4eea-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e4eea-123">None</span></span>
<span data-ttu-id="e4eea-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e4eea-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4eea-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4eea-125">OUTPUTS</span></span>

### <span data-ttu-id="e4eea-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4eea-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="e4eea-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4eea-127">NOTES</span></span>

## <span data-ttu-id="e4eea-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4eea-128">RELATED LINKS</span></span>

[<span data-ttu-id="e4eea-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e4eea-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

