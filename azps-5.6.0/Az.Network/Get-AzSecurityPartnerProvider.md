---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 99498979df259723a192bd0e2fd74ef436ae0ee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885641"
---
# <span data-ttu-id="6e84c-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6e84c-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="6e84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e84c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e84c-103">Obter um SecurityPartnerProvider do Azure</span><span class="sxs-lookup"><span data-stu-id="6e84c-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="6e84c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e84c-104">SYNTAX</span></span>

### <span data-ttu-id="6e84c-105">SecurityPartnerProviderNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e84c-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e84c-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e84c-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e84c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e84c-107">DESCRIPTION</span></span>
<span data-ttu-id="6e84c-108">O cmdlet **Get-AzSecurityPartnerProvider** obtém um SecurityPartnerProvider do Azure</span><span class="sxs-lookup"><span data-stu-id="6e84c-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="6e84c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e84c-109">EXAMPLES</span></span>

### <span data-ttu-id="6e84c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e84c-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="6e84c-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e84c-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="6e84c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e84c-112">PARAMETERS</span></span>

### <span data-ttu-id="6e84c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e84c-113">-DefaultProfile</span></span>
<span data-ttu-id="6e84c-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e84c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e84c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e84c-115">-Name</span></span>
<span data-ttu-id="6e84c-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6e84c-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e84c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e84c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e84c-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e84c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e84c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e84c-119">-ResourceId</span></span>
<span data-ttu-id="6e84c-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6e84c-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e84c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e84c-121">CommonParameters</span></span>
<span data-ttu-id="6e84c-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e84c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e84c-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e84c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e84c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e84c-124">INPUTS</span></span>

### <span data-ttu-id="6e84c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6e84c-125">System.String</span></span>

## <span data-ttu-id="6e84c-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e84c-126">OUTPUTS</span></span>

### <span data-ttu-id="6e84c-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6e84c-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="6e84c-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e84c-128">NOTES</span></span>

## <span data-ttu-id="6e84c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e84c-129">RELATED LINKS</span></span>
