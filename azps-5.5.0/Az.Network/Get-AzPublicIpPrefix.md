---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112891"
---
# <span data-ttu-id="7185c-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7185c-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="7185c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7185c-102">SYNOPSIS</span></span>
<span data-ttu-id="7185c-103">Obtém um prefixo IP público</span><span class="sxs-lookup"><span data-stu-id="7185c-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="7185c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7185c-104">SYNTAX</span></span>

### <span data-ttu-id="7185c-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7185c-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7185c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7185c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7185c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7185c-107">DESCRIPTION</span></span>
<span data-ttu-id="7185c-108">O cmdlet **Get-AzPublicIpPrefix** obtém um ou mais prefixos IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7185c-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="7185c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7185c-109">EXAMPLES</span></span>

### <span data-ttu-id="7185c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7185c-110">Example 1</span></span>
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

<span data-ttu-id="7185c-111">Este comando obtém um recurso de prefixo IP público com meuPublicIpPrefix1 no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="7185c-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="7185c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7185c-112">Example 2</span></span>
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

<span data-ttu-id="7185c-113">Esse comando obtém todos os recursos de prefixo IP públicos que começam com meuPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="7185c-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="7185c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7185c-114">PARAMETERS</span></span>

### <span data-ttu-id="7185c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7185c-115">-DefaultProfile</span></span>
<span data-ttu-id="7185c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7185c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7185c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7185c-117">-Name</span></span>
<span data-ttu-id="7185c-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7185c-118">The resource name.</span></span>

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

### <span data-ttu-id="7185c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7185c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7185c-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7185c-120">The resource group name.</span></span>

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

### <span data-ttu-id="7185c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7185c-121">-ResourceId</span></span>
<span data-ttu-id="7185c-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7185c-122">The resource Id.</span></span>

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

### <span data-ttu-id="7185c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7185c-123">CommonParameters</span></span>
<span data-ttu-id="7185c-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7185c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7185c-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7185c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7185c-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="7185c-126">INPUTS</span></span>

### <span data-ttu-id="7185c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7185c-127">System.String</span></span>

## <span data-ttu-id="7185c-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="7185c-128">OUTPUTS</span></span>

### <span data-ttu-id="7185c-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7185c-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="7185c-130">Notas</span><span class="sxs-lookup"><span data-stu-id="7185c-130">NOTES</span></span>

## <span data-ttu-id="7185c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7185c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7185c-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7185c-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="7185c-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7185c-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="7185c-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="7185c-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
