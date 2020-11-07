---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774007"
---
# <span data-ttu-id="f3037-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f3037-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="f3037-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3037-102">SYNOPSIS</span></span>
<span data-ttu-id="f3037-103">Retorna uma lista de cotas de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="f3037-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="f3037-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3037-104">SYNTAX</span></span>

### <span data-ttu-id="f3037-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3037-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f3037-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f3037-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3037-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="f3037-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3037-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3037-108">DESCRIPTION</span></span>
<span data-ttu-id="f3037-109">Retorna uma lista de cotas de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="f3037-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="f3037-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3037-110">EXAMPLES</span></span>

### <span data-ttu-id="f3037-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3037-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="f3037-112">Obter a lista de cotas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f3037-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="f3037-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3037-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="f3037-114">Obter detalhes da cota de armazenamento especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="f3037-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="f3037-115">OS</span><span class="sxs-lookup"><span data-stu-id="f3037-115">PARAMETERS</span></span>

### <span data-ttu-id="f3037-116">-Local</span><span class="sxs-lookup"><span data-stu-id="f3037-116">-Location</span></span>
<span data-ttu-id="f3037-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f3037-117">Resource location.</span></span>

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

### <span data-ttu-id="f3037-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3037-118">-Name</span></span>
<span data-ttu-id="f3037-119">O nome da cota de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f3037-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f3037-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3037-120">-ResourceId</span></span>
<span data-ttu-id="f3037-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f3037-121">The resource id.</span></span>

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

### <span data-ttu-id="f3037-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3037-122">-Skip</span></span>
<span data-ttu-id="f3037-123">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f3037-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3037-124">-Início</span><span class="sxs-lookup"><span data-stu-id="f3037-124">-Top</span></span>
<span data-ttu-id="f3037-125">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f3037-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f3037-126">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="f3037-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3037-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3037-127">CommonParameters</span></span>
<span data-ttu-id="f3037-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3037-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3037-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3037-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3037-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3037-130">INPUTS</span></span>

## <span data-ttu-id="f3037-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3037-131">OUTPUTS</span></span>

### <span data-ttu-id="f3037-132">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="f3037-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f3037-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3037-133">NOTES</span></span>

## <span data-ttu-id="f3037-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3037-134">RELATED LINKS</span></span>
