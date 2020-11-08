---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125676"
---
# <span data-ttu-id="65378-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="65378-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="65378-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65378-102">SYNOPSIS</span></span>
<span data-ttu-id="65378-103">Cria uma instância de PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="65378-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="65378-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65378-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65378-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65378-105">DESCRIPTION</span></span>
<span data-ttu-id="65378-106">O cmdlet **New-AzApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="65378-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="65378-107">Esse comando é usado com o cmdlet **set-AzApiManagement** e **New-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="65378-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="65378-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65378-108">EXAMPLES</span></span>

### <span data-ttu-id="65378-109">Exemplo 1: criar uma rede virtual e atualizar um serviço APIM existente para a VNET</span><span class="sxs-lookup"><span data-stu-id="65378-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="65378-110">Este exemplo cria uma rede virtual e, em seguida, chama o cmdlet **set-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="65378-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="65378-111">Exemplo 2: criar um serviço de gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="65378-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="65378-112">Este exemplo cria um novo serviço APIM em uma rede virtual no `External` modo</span><span class="sxs-lookup"><span data-stu-id="65378-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="65378-113">OS</span><span class="sxs-lookup"><span data-stu-id="65378-113">PARAMETERS</span></span>

### <span data-ttu-id="65378-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65378-114">-DefaultProfile</span></span>
<span data-ttu-id="65378-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65378-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65378-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="65378-116">-SubnetResourceId</span></span>
<span data-ttu-id="65378-117">Especifica a ID do recurso de sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65378-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="65378-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65378-118">CommonParameters</span></span>
<span data-ttu-id="65378-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65378-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65378-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65378-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65378-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65378-121">INPUTS</span></span>

### <span data-ttu-id="65378-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65378-122">None</span></span>

## <span data-ttu-id="65378-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65378-123">OUTPUTS</span></span>

### <span data-ttu-id="65378-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="65378-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="65378-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65378-125">NOTES</span></span>

## <span data-ttu-id="65378-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65378-126">RELATED LINKS</span></span>

<span data-ttu-id="65378-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="65378-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

