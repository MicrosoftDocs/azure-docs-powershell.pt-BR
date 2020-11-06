---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 35f63b4655b92e42eb0a7d1bae70e2ef01c57a02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430165"
---
# <span data-ttu-id="325eb-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="325eb-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="325eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="325eb-102">SYNOPSIS</span></span>
<span data-ttu-id="325eb-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="325eb-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="325eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="325eb-104">SYNTAX</span></span>

### <span data-ttu-id="325eb-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="325eb-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="325eb-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="325eb-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="325eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="325eb-107">DESCRIPTION</span></span>
<span data-ttu-id="325eb-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="325eb-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="325eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="325eb-109">EXAMPLES</span></span>

### <span data-ttu-id="325eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="325eb-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="325eb-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="325eb-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="325eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="325eb-112">PARAMETERS</span></span>

### <span data-ttu-id="325eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325eb-113">-DefaultProfile</span></span>
<span data-ttu-id="325eb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="325eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="325eb-115">-ExpandResource</span></span>
<span data-ttu-id="325eb-116">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="325eb-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="325eb-117">-Name</span></span>
<span data-ttu-id="325eb-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="325eb-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="325eb-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="325eb-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325eb-121">CommonParameters</span></span>
<span data-ttu-id="325eb-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325eb-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325eb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325eb-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="325eb-124">INPUTS</span></span>

### <span data-ttu-id="325eb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="325eb-125">System.String</span></span>

## <span data-ttu-id="325eb-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="325eb-126">OUTPUTS</span></span>

### <span data-ttu-id="325eb-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="325eb-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="325eb-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="325eb-128">NOTES</span></span>

## <span data-ttu-id="325eb-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="325eb-129">RELATED LINKS</span></span>