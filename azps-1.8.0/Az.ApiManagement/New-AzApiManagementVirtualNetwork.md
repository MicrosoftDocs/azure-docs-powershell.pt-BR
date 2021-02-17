---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 496e65438a2c0ef5f09bbf961535eaa842062f25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400885"
---
# <span data-ttu-id="3434f-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3434f-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3434f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3434f-102">SYNOPSIS</span></span>
<span data-ttu-id="3434f-103">Cria uma instância do PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="3434f-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="3434f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3434f-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3434f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3434f-105">DESCRIPTION</span></span>
<span data-ttu-id="3434f-106">O cmdlet **New-AzApiManagementVirtualNetwork** é um comando auxiliar para criar uma instância de **PsApiManagementVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="3434f-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="3434f-107">Esse comando é usado com **o cmdlet Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="3434f-107">This command is used with **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="3434f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3434f-108">EXAMPLES</span></span>

### <span data-ttu-id="3434f-109">Exemplo 1: Criar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="3434f-109">Example 1: Create a virtual network</span></span>
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
PS C:\>Set-AzApiManagement -ApiManagement $service
```

<span data-ttu-id="3434f-110">Este exemplo cria uma rede virtual e chama o cmdlet **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="3434f-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="3434f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3434f-111">PARAMETERS</span></span>

### <span data-ttu-id="3434f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3434f-112">-DefaultProfile</span></span>
<span data-ttu-id="3434f-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3434f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3434f-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="3434f-114">-SubnetResourceId</span></span>
<span data-ttu-id="3434f-115">Especifica a ID de recurso da sub-rede da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3434f-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="3434f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3434f-116">CommonParameters</span></span>
<span data-ttu-id="3434f-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3434f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3434f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3434f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3434f-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="3434f-119">INPUTS</span></span>

### <span data-ttu-id="3434f-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3434f-120">None</span></span>

## <span data-ttu-id="3434f-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="3434f-121">OUTPUTS</span></span>

### <span data-ttu-id="3434f-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3434f-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="3434f-123">Notas</span><span class="sxs-lookup"><span data-stu-id="3434f-123">NOTES</span></span>

## <span data-ttu-id="3434f-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3434f-124">RELATED LINKS</span></span>

[<span data-ttu-id="3434f-125">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3434f-125">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

