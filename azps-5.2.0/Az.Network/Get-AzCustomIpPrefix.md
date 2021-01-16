---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256580"
---
# <span data-ttu-id="c8212-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c8212-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8212-102">SYNOPSIS</span></span>
<span data-ttu-id="c8212-103">Obtém um recurso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="c8212-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8212-104">SYNTAX</span></span>

### <span data-ttu-id="c8212-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8212-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8212-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8212-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8212-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8212-107">DESCRIPTION</span></span>
<span data-ttu-id="c8212-108">O cmdlet **Get-AzCustomIpPrefix** Obtém uma ou mais CustomIpPrefixes de acordo com o conjunto de parâmetros de entrada</span><span class="sxs-lookup"><span data-stu-id="c8212-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="c8212-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8212-109">EXAMPLES</span></span>

### <span data-ttu-id="c8212-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8212-110">Example 1</span></span>
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

<span data-ttu-id="c8212-111">Esse comando obtém um recurso CustomIpPrefix chamado myCustomIpPrefix no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="c8212-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="c8212-112">OS</span><span class="sxs-lookup"><span data-stu-id="c8212-112">PARAMETERS</span></span>

### <span data-ttu-id="c8212-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8212-113">-DefaultProfile</span></span>
<span data-ttu-id="c8212-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8212-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8212-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8212-115">-Name</span></span>
<span data-ttu-id="c8212-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8212-116">The resource name.</span></span>

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

### <span data-ttu-id="c8212-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8212-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8212-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8212-118">The resource group name.</span></span>

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

### <span data-ttu-id="c8212-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8212-119">-ResourceId</span></span>
<span data-ttu-id="c8212-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8212-120">The resource id.</span></span>

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

### <span data-ttu-id="c8212-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8212-121">CommonParameters</span></span>
<span data-ttu-id="c8212-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8212-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8212-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8212-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8212-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8212-124">INPUTS</span></span>

### <span data-ttu-id="c8212-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c8212-125">System.String</span></span>

## <span data-ttu-id="c8212-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8212-126">OUTPUTS</span></span>

### <span data-ttu-id="c8212-127">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c8212-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8212-128">NOTES</span></span>

## <span data-ttu-id="c8212-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8212-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8212-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="c8212-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="c8212-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8212-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)