---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425814"
---
# <span data-ttu-id="abcb4-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="abcb4-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="abcb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abcb4-102">SYNOPSIS</span></span>
<span data-ttu-id="abcb4-103">Listar todas as cotas.</span><span class="sxs-lookup"><span data-stu-id="abcb4-103">List all quotas.</span></span>

## <span data-ttu-id="abcb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abcb4-104">SYNTAX</span></span>

### <span data-ttu-id="abcb4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="abcb4-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="abcb4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="abcb4-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="abcb4-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="abcb4-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="abcb4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abcb4-108">DESCRIPTION</span></span>
<span data-ttu-id="abcb4-109">Listar todas as cotas.</span><span class="sxs-lookup"><span data-stu-id="abcb4-109">List all quotas.</span></span>
<span data-ttu-id="abcb4-110">Limite a lista passando um nome ou um filtro.</span><span class="sxs-lookup"><span data-stu-id="abcb4-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="abcb4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abcb4-111">EXAMPLES</span></span>

### <span data-ttu-id="abcb4-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="abcb4-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="abcb4-113">Lista todas as cotas de rede.</span><span class="sxs-lookup"><span data-stu-id="abcb4-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="abcb4-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="abcb4-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="abcb4-115">Obtém a cota de rede especificada.</span><span class="sxs-lookup"><span data-stu-id="abcb4-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="abcb4-116">OS</span><span class="sxs-lookup"><span data-stu-id="abcb4-116">PARAMETERS</span></span>

### <span data-ttu-id="abcb4-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="abcb4-117">-Filter</span></span>
<span data-ttu-id="abcb4-118">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="abcb4-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb4-119">-Local</span><span class="sxs-lookup"><span data-stu-id="abcb4-119">-Location</span></span>
<span data-ttu-id="abcb4-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="abcb4-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="abcb4-121">-Name</span></span>
<span data-ttu-id="abcb4-122">Nome do recurso de cota da rede.</span><span class="sxs-lookup"><span data-stu-id="abcb4-122">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcb4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abcb4-123">-ResourceId</span></span>
<span data-ttu-id="abcb4-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="abcb4-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcb4-125">CommonParameters</span></span>
<span data-ttu-id="abcb4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abcb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcb4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcb4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcb4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abcb4-128">INPUTS</span></span>

## <span data-ttu-id="abcb4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abcb4-129">OUTPUTS</span></span>

### <span data-ttu-id="abcb4-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="abcb4-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="abcb4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abcb4-131">NOTES</span></span>

## <span data-ttu-id="abcb4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abcb4-132">RELATED LINKS</span></span>

