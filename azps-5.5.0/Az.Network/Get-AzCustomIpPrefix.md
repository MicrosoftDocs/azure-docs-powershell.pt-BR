---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117452"
---
# <span data-ttu-id="d7988-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="d7988-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7988-102">SYNOPSIS</span></span>
<span data-ttu-id="d7988-103">Obtém um recurso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="d7988-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7988-104">SYNTAX</span></span>

### <span data-ttu-id="d7988-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7988-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7988-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7988-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7988-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7988-107">DESCRIPTION</span></span>
<span data-ttu-id="d7988-108">O cmdlet **Get-AzCustomIpPrefix** obtém um ou mais CustomIpPrefixes de acordo com o conjunto de parâmetros de entrada</span><span class="sxs-lookup"><span data-stu-id="d7988-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="d7988-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7988-109">EXAMPLES</span></span>

### <span data-ttu-id="d7988-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7988-110">Example 1</span></span>
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

<span data-ttu-id="d7988-111">Este comando obtém um recurso CustomIpPrefix chamado myCustomIpPrefix no grupo de recursos myRg</span><span class="sxs-lookup"><span data-stu-id="d7988-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="d7988-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7988-112">PARAMETERS</span></span>

### <span data-ttu-id="d7988-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7988-113">-DefaultProfile</span></span>
<span data-ttu-id="d7988-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7988-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7988-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7988-115">-Name</span></span>
<span data-ttu-id="d7988-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d7988-116">The resource name.</span></span>

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

### <span data-ttu-id="d7988-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7988-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7988-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7988-118">The resource group name.</span></span>

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

### <span data-ttu-id="d7988-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7988-119">-ResourceId</span></span>
<span data-ttu-id="d7988-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d7988-120">The resource id.</span></span>

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

### <span data-ttu-id="d7988-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7988-121">CommonParameters</span></span>
<span data-ttu-id="d7988-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7988-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7988-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7988-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7988-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7988-124">INPUTS</span></span>

### <span data-ttu-id="d7988-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d7988-125">System.String</span></span>

## <span data-ttu-id="d7988-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7988-126">OUTPUTS</span></span>

### <span data-ttu-id="d7988-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="d7988-128">Notas</span><span class="sxs-lookup"><span data-stu-id="d7988-128">NOTES</span></span>

## <span data-ttu-id="d7988-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7988-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7988-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="d7988-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="d7988-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d7988-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)