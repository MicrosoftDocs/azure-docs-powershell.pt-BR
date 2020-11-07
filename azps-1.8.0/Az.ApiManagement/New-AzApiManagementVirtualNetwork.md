---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771400"
---
# <span data-ttu-id="458db-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="458db-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="458db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="458db-102">SYNOPSIS</span></span>
<span data-ttu-id="458db-103">Cria uma instância de PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="458db-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="458db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="458db-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="458db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="458db-105">DESCRIPTION</span></span>
<span data-ttu-id="458db-106">O cmdlet **New-AzApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="458db-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="458db-107">Esse comando é usado com o cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="458db-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="458db-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="458db-108">EXAMPLES</span></span>

### <span data-ttu-id="458db-109">Exemplo 1: criar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="458db-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="458db-110">Este exemplo cria uma rede virtual e, em seguida, chama o cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="458db-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="458db-111">OS</span><span class="sxs-lookup"><span data-stu-id="458db-111">PARAMETERS</span></span>

### <span data-ttu-id="458db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458db-112">-DefaultProfile</span></span>
<span data-ttu-id="458db-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="458db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458db-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="458db-114">-SubnetResourceId</span></span>
<span data-ttu-id="458db-115">Especifica a ID do recurso de sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="458db-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="458db-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458db-116">CommonParameters</span></span>
<span data-ttu-id="458db-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458db-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458db-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458db-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458db-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="458db-119">INPUTS</span></span>

### <span data-ttu-id="458db-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="458db-120">None</span></span>

## <span data-ttu-id="458db-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="458db-121">OUTPUTS</span></span>

### <span data-ttu-id="458db-122">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="458db-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="458db-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="458db-123">NOTES</span></span>

## <span data-ttu-id="458db-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="458db-124">RELATED LINKS</span></span>

[<span data-ttu-id="458db-125">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="458db-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

