---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110565"
---
# <span data-ttu-id="fe903-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="fe903-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe903-102">SYNOPSIS</span></span>
<span data-ttu-id="fe903-103">Obtém um recurso de nível superior do perfil de rede existente</span><span class="sxs-lookup"><span data-stu-id="fe903-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="fe903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe903-104">SYNTAX</span></span>

### <span data-ttu-id="fe903-105">GetByResourceNameNoExpandParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe903-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe903-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe903-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe903-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe903-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe903-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe903-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe903-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe903-109">DESCRIPTION</span></span>
<span data-ttu-id="fe903-110">O cmdlet **Get-AzNetworkProfile** recupera um recurso de nível superior de perfil de rede existente</span><span class="sxs-lookup"><span data-stu-id="fe903-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="fe903-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe903-111">EXAMPLES</span></span>

### <span data-ttu-id="fe903-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe903-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="fe903-113">Isso recupera o perfil de rede NP1 na Rg1 de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fe903-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="fe903-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fe903-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="fe903-115">Isso recupera os perfis de rede que começam com "np"</span><span class="sxs-lookup"><span data-stu-id="fe903-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="fe903-116">OS</span><span class="sxs-lookup"><span data-stu-id="fe903-116">PARAMETERS</span></span>

### <span data-ttu-id="fe903-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-117">-DefaultProfile</span></span>
<span data-ttu-id="fe903-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe903-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe903-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fe903-119">-ExpandResource</span></span>
<span data-ttu-id="fe903-120">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="fe903-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe903-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe903-121">-Name</span></span>
<span data-ttu-id="fe903-122">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fe903-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fe903-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe903-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe903-124">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fe903-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fe903-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe903-125">-ResourceId</span></span>
<span data-ttu-id="fe903-126">A ID do perfil de rede do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fe903-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe903-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe903-127">CommonParameters</span></span>
<span data-ttu-id="fe903-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe903-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe903-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe903-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe903-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe903-130">INPUTS</span></span>

### <span data-ttu-id="fe903-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fe903-131">System.String</span></span>

## <span data-ttu-id="fe903-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe903-132">OUTPUTS</span></span>

### <span data-ttu-id="fe903-133">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="fe903-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe903-134">NOTES</span></span>

## <span data-ttu-id="fe903-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe903-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe903-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="fe903-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="fe903-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe903-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
