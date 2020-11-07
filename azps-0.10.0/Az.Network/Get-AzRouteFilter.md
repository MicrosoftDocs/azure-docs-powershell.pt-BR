---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775487"
---
# <span data-ttu-id="fe6c8-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe6c8-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="fe6c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe6c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6c8-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="fe6c8-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="fe6c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe6c8-104">SYNTAX</span></span>

### <span data-ttu-id="fe6c8-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="fe6c8-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe6c8-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="fe6c8-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe6c8-107">DESCRIPTION</span></span>
<span data-ttu-id="fe6c8-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="fe6c8-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="fe6c8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe6c8-109">EXAMPLES</span></span>

### <span data-ttu-id="fe6c8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe6c8-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fe6c8-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="fe6c8-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="fe6c8-112">OS</span><span class="sxs-lookup"><span data-stu-id="fe6c8-112">PARAMETERS</span></span>

### <span data-ttu-id="fe6c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6c8-113">-DefaultProfile</span></span>
<span data-ttu-id="fe6c8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe6c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c8-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fe6c8-115">-ExpandResource</span></span>
<span data-ttu-id="fe6c8-116">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="fe6c8-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe6c8-117">-Name</span></span>
<span data-ttu-id="fe6c8-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6c8-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe6c8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe6c8-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6c8-121">CommonParameters</span></span>
<span data-ttu-id="fe6c8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6c8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6c8-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6c8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6c8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe6c8-124">INPUTS</span></span>

### <span data-ttu-id="fe6c8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fe6c8-125">System.String</span></span>

## <span data-ttu-id="fe6c8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe6c8-126">OUTPUTS</span></span>

### <span data-ttu-id="fe6c8-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fe6c8-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fe6c8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe6c8-128">NOTES</span></span>

## <span data-ttu-id="fe6c8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe6c8-129">RELATED LINKS</span></span>

