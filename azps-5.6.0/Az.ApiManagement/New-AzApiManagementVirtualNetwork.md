---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: a714730a416d7554cba53e96428c9813fe4e720d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886281"
---
# <span data-ttu-id="01367-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="01367-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="01367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01367-102">SYNOPSIS</span></span>
<span data-ttu-id="01367-103">Cria uma instância de PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="01367-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="01367-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="01367-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01367-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="01367-105">DESCRIPTION</span></span>
<span data-ttu-id="01367-106">O cmdlet **New-AzApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="01367-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="01367-107">Este comando é usado com **Set-AzApiManagement** **e cmdlet New-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="01367-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="01367-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01367-108">EXAMPLES</span></span>

### <span data-ttu-id="01367-109">Exemplo 1: Criar uma rede virtual e atualizar um serviço APIM existente na VNET</span><span class="sxs-lookup"><span data-stu-id="01367-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="01367-110">Este exemplo cria uma rede virtual e chama o cmdlet **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="01367-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="01367-111">Exemplo 2: Criar um serviço de Gerenciamento de API para uma rede virtual externa</span><span class="sxs-lookup"><span data-stu-id="01367-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="01367-112">Este exemplo cria um novo serviço APIM em uma Rede Virtual no `External` modo</span><span class="sxs-lookup"><span data-stu-id="01367-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="01367-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="01367-113">PARAMETERS</span></span>

### <span data-ttu-id="01367-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01367-114">-DefaultProfile</span></span>
<span data-ttu-id="01367-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="01367-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01367-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="01367-116">-SubnetResourceId</span></span>
<span data-ttu-id="01367-117">Especifica a ID do recurso de sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="01367-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="01367-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01367-118">CommonParameters</span></span>
<span data-ttu-id="01367-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01367-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01367-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01367-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01367-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01367-121">INPUTS</span></span>

### <span data-ttu-id="01367-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="01367-122">None</span></span>

## <span data-ttu-id="01367-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="01367-123">OUTPUTS</span></span>

### <span data-ttu-id="01367-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="01367-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="01367-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="01367-125">NOTES</span></span>

## <span data-ttu-id="01367-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01367-126">RELATED LINKS</span></span>

<span data-ttu-id="01367-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="01367-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

