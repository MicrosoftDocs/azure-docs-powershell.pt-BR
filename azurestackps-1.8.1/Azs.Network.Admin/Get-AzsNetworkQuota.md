---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775087"
---
# <span data-ttu-id="638d7-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="638d7-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="638d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="638d7-102">SYNOPSIS</span></span>
<span data-ttu-id="638d7-103">Listar todas as cotas.</span><span class="sxs-lookup"><span data-stu-id="638d7-103">List all quotas.</span></span>

## <span data-ttu-id="638d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="638d7-104">SYNTAX</span></span>

### <span data-ttu-id="638d7-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="638d7-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="638d7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="638d7-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="638d7-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="638d7-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="638d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="638d7-108">DESCRIPTION</span></span>
<span data-ttu-id="638d7-109">Listar todas as cotas.</span><span class="sxs-lookup"><span data-stu-id="638d7-109">List all quotas.</span></span>
<span data-ttu-id="638d7-110">Limite a lista passando um nome ou um filtro.</span><span class="sxs-lookup"><span data-stu-id="638d7-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="638d7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="638d7-111">EXAMPLES</span></span>

### <span data-ttu-id="638d7-112">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="638d7-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="638d7-113">Lista todas as cotas de rede.</span><span class="sxs-lookup"><span data-stu-id="638d7-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="638d7-114">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="638d7-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="638d7-115">Obtém a cota de rede especificada.</span><span class="sxs-lookup"><span data-stu-id="638d7-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="638d7-116">OS</span><span class="sxs-lookup"><span data-stu-id="638d7-116">PARAMETERS</span></span>

### <span data-ttu-id="638d7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="638d7-117">-Name</span></span>
<span data-ttu-id="638d7-118">Nome do recurso de cota da rede.</span><span class="sxs-lookup"><span data-stu-id="638d7-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="638d7-119">-Local</span><span class="sxs-lookup"><span data-stu-id="638d7-119">-Location</span></span>
<span data-ttu-id="638d7-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="638d7-120">Location of the resource.</span></span>

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

### <span data-ttu-id="638d7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="638d7-121">-ResourceId</span></span>
<span data-ttu-id="638d7-122">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="638d7-122">The resource id.</span></span>

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

### <span data-ttu-id="638d7-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="638d7-123">-Filter</span></span>
<span data-ttu-id="638d7-124">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="638d7-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="638d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638d7-125">CommonParameters</span></span>
<span data-ttu-id="638d7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638d7-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638d7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638d7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="638d7-128">INPUTS</span></span>

## <span data-ttu-id="638d7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="638d7-129">OUTPUTS</span></span>

### <span data-ttu-id="638d7-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="638d7-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="638d7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="638d7-131">NOTES</span></span>

## <span data-ttu-id="638d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="638d7-132">RELATED LINKS</span></span>
