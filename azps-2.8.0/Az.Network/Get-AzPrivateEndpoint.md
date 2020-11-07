---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 59f8b74a9815820b1ace1e9d7defeb5b9dd85efa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771986"
---
# <span data-ttu-id="e8a6e-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8a6e-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="e8a6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a6e-103">Obter um ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e8a6e-103">Get a private endpoint</span></span>

## <span data-ttu-id="e8a6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8a6e-104">SYNTAX</span></span>

### <span data-ttu-id="e8a6e-105">NOEXPAND (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8a6e-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8a6e-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="e8a6e-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a6e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="e8a6e-108">O cmdlet **Get-AzPrivateEndpoint** Obtém um ou mais pontos de extremidade privados.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="e8a6e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a6e-110">1: recuperar um ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e8a6e-110">1: Retrieve a private endpoint</span></span>
```
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="e8a6e-111">Esse comando obtém o ponto de extremidade privado chamado MyPrivateEndpoint1 na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e8a6e-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="e8a6e-112">2: listar todos os pontos de extremidade particulares no MySource</span><span class="sxs-lookup"><span data-stu-id="e8a6e-112">2: List all private endpoints in ResourceGroup</span></span>
```
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="e8a6e-113">Esse comando obtém todos os pontos de extremidade particulares na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e8a6e-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="e8a6e-114">OS</span><span class="sxs-lookup"><span data-stu-id="e8a6e-114">PARAMETERS</span></span>

### <span data-ttu-id="e8a6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a6e-115">-DefaultProfile</span></span>
<span data-ttu-id="e8a6e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a6e-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="e8a6e-117">-ExpandResource</span></span>
<span data-ttu-id="e8a6e-118">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a6e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8a6e-119">-Name</span></span>
<span data-ttu-id="e8a6e-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8a6e-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a6e-123">CommonParameters</span></span>
<span data-ttu-id="e8a6e-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a6e-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8a6e-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a6e-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8a6e-126">INPUTS</span></span>

### <span data-ttu-id="e8a6e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8a6e-127">System.String</span></span>

## <span data-ttu-id="e8a6e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8a6e-128">OUTPUTS</span></span>

### <span data-ttu-id="e8a6e-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8a6e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e8a6e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8a6e-130">NOTES</span></span>

## <span data-ttu-id="e8a6e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8a6e-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8a6e-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8a6e-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="e8a6e-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8a6e-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)