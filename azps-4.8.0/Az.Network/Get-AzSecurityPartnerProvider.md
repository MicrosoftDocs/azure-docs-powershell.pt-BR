---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110538"
---
# <span data-ttu-id="42684-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="42684-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="42684-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42684-102">SYNOPSIS</span></span>
<span data-ttu-id="42684-103">Obter um SecurityPartnerProvider do Azure</span><span class="sxs-lookup"><span data-stu-id="42684-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="42684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42684-104">SYNTAX</span></span>

### <span data-ttu-id="42684-105">SecurityPartnerProviderNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="42684-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42684-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42684-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42684-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42684-107">DESCRIPTION</span></span>
<span data-ttu-id="42684-108">O cmdlet **Get-AzSecurityPartnerProvider** Obtém um SecurityPartnerProvider do Azure</span><span class="sxs-lookup"><span data-stu-id="42684-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="42684-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42684-109">EXAMPLES</span></span>

### <span data-ttu-id="42684-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42684-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="42684-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="42684-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="42684-112">OS</span><span class="sxs-lookup"><span data-stu-id="42684-112">PARAMETERS</span></span>

### <span data-ttu-id="42684-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42684-113">-DefaultProfile</span></span>
<span data-ttu-id="42684-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42684-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42684-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="42684-115">-Name</span></span>
<span data-ttu-id="42684-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="42684-116">The resource name.</span></span>

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

### <span data-ttu-id="42684-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42684-117">-ResourceGroupName</span></span>
<span data-ttu-id="42684-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42684-118">The resource group name.</span></span>

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

### <span data-ttu-id="42684-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42684-119">-ResourceId</span></span>
<span data-ttu-id="42684-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="42684-120">The resource Id.</span></span>

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

### <span data-ttu-id="42684-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42684-121">CommonParameters</span></span>
<span data-ttu-id="42684-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42684-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42684-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42684-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42684-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42684-124">INPUTS</span></span>

### <span data-ttu-id="42684-125">System. String</span><span class="sxs-lookup"><span data-stu-id="42684-125">System.String</span></span>

## <span data-ttu-id="42684-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42684-126">OUTPUTS</span></span>

### <span data-ttu-id="42684-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="42684-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="42684-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42684-128">NOTES</span></span>

## <span data-ttu-id="42684-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42684-129">RELATED LINKS</span></span>
