---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954883"
---
# <span data-ttu-id="20bea-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="20bea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20bea-102">SYNOPSIS</span></span>
<span data-ttu-id="20bea-103">Obtém um recurso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="20bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20bea-104">SYNTAX</span></span>

### <span data-ttu-id="20bea-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="20bea-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20bea-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20bea-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20bea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20bea-107">DESCRIPTION</span></span>
<span data-ttu-id="20bea-108">O cmdlet **Get-AzCustomIpPrefix** Obtém uma ou mais CustomIpPrefixes de acordo com o conjunto de parâmetros de entrada</span><span class="sxs-lookup"><span data-stu-id="20bea-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="20bea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20bea-109">EXAMPLES</span></span>

### <span data-ttu-id="20bea-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20bea-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="20bea-111">Esse comando obtém um recurso CustomIpPrefix chamado myCustomIpPrefix no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="20bea-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="20bea-112">OS</span><span class="sxs-lookup"><span data-stu-id="20bea-112">PARAMETERS</span></span>

### <span data-ttu-id="20bea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20bea-113">-DefaultProfile</span></span>
<span data-ttu-id="20bea-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20bea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20bea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="20bea-115">-Name</span></span>
<span data-ttu-id="20bea-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="20bea-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20bea-117">-ResourceGroupName</span></span>
<span data-ttu-id="20bea-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20bea-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bea-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20bea-119">-ResourceId</span></span>
<span data-ttu-id="20bea-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="20bea-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bea-121">CommonParameters</span></span>
<span data-ttu-id="20bea-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20bea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bea-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20bea-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bea-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20bea-124">INPUTS</span></span>

### <span data-ttu-id="20bea-125">System. String</span><span class="sxs-lookup"><span data-stu-id="20bea-125">System.String</span></span>

## <span data-ttu-id="20bea-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20bea-126">OUTPUTS</span></span>

### <span data-ttu-id="20bea-127">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="20bea-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20bea-128">NOTES</span></span>

## <span data-ttu-id="20bea-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20bea-129">RELATED LINKS</span></span>

[<span data-ttu-id="20bea-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="20bea-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="20bea-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20bea-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)