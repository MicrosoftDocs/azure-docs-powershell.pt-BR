---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: a1a134905795123311d1ce0fb89e461678f9f41a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771980"
---
# <span data-ttu-id="f88ab-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f88ab-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f88ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f88ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f88ab-103">Obtém um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="f88ab-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="f88ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f88ab-104">SYNTAX</span></span>

### <span data-ttu-id="f88ab-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f88ab-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f88ab-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f88ab-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88ab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f88ab-107">DESCRIPTION</span></span>
<span data-ttu-id="f88ab-108">O cmdlet **Get-AzPublicIpPrefix** Obtém um ou mais prefixos IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f88ab-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="f88ab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f88ab-109">EXAMPLES</span></span>

### <span data-ttu-id="f88ab-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f88ab-110">Example 1</span></span>
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
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="f88ab-111">Este comando obtém um recurso de prefixo de IP público com o myPublicIpPrefix1 no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="f88ab-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="f88ab-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f88ab-112">Example 2</span></span>
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
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="f88ab-113">Esse comando obtém todos os recursos de prefixo de IP público que começam com myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="f88ab-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="f88ab-114">OS</span><span class="sxs-lookup"><span data-stu-id="f88ab-114">PARAMETERS</span></span>

### <span data-ttu-id="f88ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88ab-115">-DefaultProfile</span></span>
<span data-ttu-id="f88ab-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f88ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88ab-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f88ab-117">-Name</span></span>
<span data-ttu-id="f88ab-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f88ab-118">The resource name.</span></span>

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

### <span data-ttu-id="f88ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="f88ab-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f88ab-120">The resource group name.</span></span>

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

### <span data-ttu-id="f88ab-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f88ab-121">-ResourceId</span></span>
<span data-ttu-id="f88ab-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f88ab-122">The resource Id.</span></span>

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

### <span data-ttu-id="f88ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88ab-123">CommonParameters</span></span>
<span data-ttu-id="f88ab-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88ab-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f88ab-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88ab-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f88ab-126">INPUTS</span></span>

### <span data-ttu-id="f88ab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f88ab-127">System.String</span></span>

## <span data-ttu-id="f88ab-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f88ab-128">OUTPUTS</span></span>

### <span data-ttu-id="f88ab-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f88ab-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f88ab-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f88ab-130">NOTES</span></span>

## <span data-ttu-id="f88ab-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f88ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="f88ab-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f88ab-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="f88ab-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f88ab-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="f88ab-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f88ab-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
