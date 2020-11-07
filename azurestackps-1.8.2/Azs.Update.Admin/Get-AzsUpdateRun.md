---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946934"
---
# <span data-ttu-id="654bb-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="654bb-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="654bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="654bb-102">SYNOPSIS</span></span>
<span data-ttu-id="654bb-103">Obter a lista de execuções de atualização.</span><span class="sxs-lookup"><span data-stu-id="654bb-103">Get the list of update runs.</span></span>

## <span data-ttu-id="654bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="654bb-104">SYNTAX</span></span>

### <span data-ttu-id="654bb-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="654bb-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="654bb-106">Obter</span><span class="sxs-lookup"><span data-stu-id="654bb-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="654bb-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="654bb-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="654bb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="654bb-108">DESCRIPTION</span></span>
<span data-ttu-id="654bb-109">Obter a lista de execuções de atualização.</span><span class="sxs-lookup"><span data-stu-id="654bb-109">Get the list of update runs.</span></span> <span data-ttu-id="654bb-110">As instâncias dos objetos UpdateRun retornadas podem ser canalizadas para Restart-AzsUpdateRun, quando aplicável.</span><span class="sxs-lookup"><span data-stu-id="654bb-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="654bb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="654bb-111">EXAMPLES</span></span>

### <span data-ttu-id="654bb-112">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="654bb-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="654bb-113">Obter uma lista de todas as tentativas de aplicar uma atualização específica.</span><span class="sxs-lookup"><span data-stu-id="654bb-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="654bb-114">OS</span><span class="sxs-lookup"><span data-stu-id="654bb-114">PARAMETERS</span></span>

### <span data-ttu-id="654bb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="654bb-115">-Name</span></span>
<span data-ttu-id="654bb-116">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="654bb-116">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654bb-117">-Updatename</span><span class="sxs-lookup"><span data-stu-id="654bb-117">-UpdateName</span></span>
<span data-ttu-id="654bb-118">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="654bb-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654bb-119">-Local</span><span class="sxs-lookup"><span data-stu-id="654bb-119">-Location</span></span>
<span data-ttu-id="654bb-120">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="654bb-120">The name of the update location.</span></span>

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

### <span data-ttu-id="654bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="654bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="654bb-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="654bb-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="654bb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="654bb-123">-ResourceId</span></span>
<span data-ttu-id="654bb-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="654bb-124">The resource id.</span></span>

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

### <span data-ttu-id="654bb-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="654bb-125">-Skip</span></span>
<span data-ttu-id="654bb-126">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="654bb-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="654bb-127">-Início</span><span class="sxs-lookup"><span data-stu-id="654bb-127">-Top</span></span>
<span data-ttu-id="654bb-128">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="654bb-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="654bb-129">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="654bb-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="654bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654bb-130">CommonParameters</span></span>
<span data-ttu-id="654bb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654bb-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654bb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654bb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="654bb-133">INPUTS</span></span>

## <span data-ttu-id="654bb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="654bb-134">OUTPUTS</span></span>

### <span data-ttu-id="654bb-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="654bb-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="654bb-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="654bb-136">NOTES</span></span>

## <span data-ttu-id="654bb-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="654bb-137">RELATED LINKS</span></span>
