---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428146"
---
# <span data-ttu-id="92e12-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="92e12-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="92e12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92e12-102">SYNOPSIS</span></span>
<span data-ttu-id="92e12-103">Obtém um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="92e12-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="92e12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92e12-104">SYNTAX</span></span>

### <span data-ttu-id="92e12-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="92e12-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92e12-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e12-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e12-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92e12-107">DESCRIPTION</span></span>
<span data-ttu-id="92e12-108">O cmdlet **Get-AzPublicIpPrefix** Obtém um ou mais prefixos IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e12-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="92e12-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92e12-109">EXAMPLES</span></span>

### <span data-ttu-id="92e12-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92e12-110">Example 1</span></span>
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

<span data-ttu-id="92e12-111">Este comando obtém um recurso de prefixo de IP público com o myPublicIpPrefix1 no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="92e12-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="92e12-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="92e12-112">Example 2</span></span>
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

<span data-ttu-id="92e12-113">Esse comando obtém todos os recursos de prefixo de IP público que começam com myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="92e12-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="92e12-114">OS</span><span class="sxs-lookup"><span data-stu-id="92e12-114">PARAMETERS</span></span>

### <span data-ttu-id="92e12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e12-115">-DefaultProfile</span></span>
<span data-ttu-id="92e12-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92e12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e12-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="92e12-117">-Name</span></span>
<span data-ttu-id="92e12-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="92e12-118">The resource name.</span></span>

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

### <span data-ttu-id="92e12-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e12-119">-ResourceGroupName</span></span>
<span data-ttu-id="92e12-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e12-120">The resource group name.</span></span>

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

### <span data-ttu-id="92e12-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92e12-121">-ResourceId</span></span>
<span data-ttu-id="92e12-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="92e12-122">The resource Id.</span></span>

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

### <span data-ttu-id="92e12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e12-123">CommonParameters</span></span>
<span data-ttu-id="92e12-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e12-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e12-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e12-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92e12-126">INPUTS</span></span>

### <span data-ttu-id="92e12-127">System. String</span><span class="sxs-lookup"><span data-stu-id="92e12-127">System.String</span></span>

## <span data-ttu-id="92e12-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92e12-128">OUTPUTS</span></span>

### <span data-ttu-id="92e12-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="92e12-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="92e12-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92e12-130">NOTES</span></span>

## <span data-ttu-id="92e12-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92e12-131">RELATED LINKS</span></span>

[<span data-ttu-id="92e12-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="92e12-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="92e12-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="92e12-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="92e12-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="92e12-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
