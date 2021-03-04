---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885649"
---
# <span data-ttu-id="f6821-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f6821-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f6821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6821-102">SYNOPSIS</span></span>
<span data-ttu-id="f6821-103">Obtém um prefixo IP público</span><span class="sxs-lookup"><span data-stu-id="f6821-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="f6821-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6821-104">SYNTAX</span></span>

### <span data-ttu-id="f6821-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6821-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6821-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6821-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6821-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6821-107">DESCRIPTION</span></span>
<span data-ttu-id="f6821-108">O cmdlet **Get-AzPublicIpPrefix** obtém um ou mais prefixos IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6821-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="f6821-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6821-109">EXAMPLES</span></span>

### <span data-ttu-id="f6821-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6821-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="f6821-111">Este comando obtém um recurso de prefixo IP público com myPublicIpPrefix1 no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="f6821-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="f6821-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f6821-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="f6821-113">Este comando obtém todos os recursos de prefixo IP públicos que começam com myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="f6821-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="f6821-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6821-114">PARAMETERS</span></span>

### <span data-ttu-id="f6821-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6821-115">-DefaultProfile</span></span>
<span data-ttu-id="f6821-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6821-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6821-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f6821-117">-Name</span></span>
<span data-ttu-id="f6821-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6821-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f6821-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6821-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6821-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6821-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f6821-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6821-121">-ResourceId</span></span>
<span data-ttu-id="f6821-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6821-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6821-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6821-123">CommonParameters</span></span>
<span data-ttu-id="f6821-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6821-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6821-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6821-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6821-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6821-126">INPUTS</span></span>

### <span data-ttu-id="f6821-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f6821-127">System.String</span></span>

## <span data-ttu-id="f6821-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6821-128">OUTPUTS</span></span>

### <span data-ttu-id="f6821-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f6821-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f6821-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6821-130">NOTES</span></span>

## <span data-ttu-id="f6821-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6821-131">RELATED LINKS</span></span>

[<span data-ttu-id="f6821-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f6821-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="f6821-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f6821-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="f6821-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f6821-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
