---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426035"
---
# <span data-ttu-id="cb0c9-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="cb0c9-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="cb0c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb0c9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0c9-103">Obter a lista de atualizações disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-103">Get the list of available updates.</span></span>

## <span data-ttu-id="cb0c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb0c9-104">SYNTAX</span></span>

### <span data-ttu-id="cb0c9-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb0c9-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb0c9-106">Obter</span><span class="sxs-lookup"><span data-stu-id="cb0c9-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cb0c9-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="cb0c9-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cb0c9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb0c9-108">DESCRIPTION</span></span>
<span data-ttu-id="cb0c9-109">Obter a lista de atualizações disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-109">Get the list of available updates.</span></span> <span data-ttu-id="cb0c9-110">As atualizações retornadas deste módulo podem ser canalizadas para ' Install-AzsUpdate ', se aplicável.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="cb0c9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb0c9-111">EXAMPLES</span></span>

### <span data-ttu-id="cb0c9-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb0c9-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="cb0c9-113">Obter a lista de atualizações disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-113">Get the list of available updates.</span></span>

### <span data-ttu-id="cb0c9-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb0c9-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="cb0c9-115">Obtenha a atualização específica.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-115">Get the specific update.</span></span>

## <span data-ttu-id="cb0c9-116">OS</span><span class="sxs-lookup"><span data-stu-id="cb0c9-116">PARAMETERS</span></span>

### <span data-ttu-id="cb0c9-117">-Local</span><span class="sxs-lookup"><span data-stu-id="cb0c9-117">-Location</span></span>
<span data-ttu-id="cb0c9-118">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-118">The name of the update location.</span></span>

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

### <span data-ttu-id="cb0c9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb0c9-119">-Name</span></span>
<span data-ttu-id="cb0c9-120">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-120">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb0c9-122">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="cb0c9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb0c9-123">-ResourceId</span></span>
<span data-ttu-id="cb0c9-124">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-124">The resource id.</span></span>

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

### <span data-ttu-id="cb0c9-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="cb0c9-125">-Skip</span></span>
<span data-ttu-id="cb0c9-126">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cb0c9-127">-Início</span><span class="sxs-lookup"><span data-stu-id="cb0c9-127">-Top</span></span>
<span data-ttu-id="cb0c9-128">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cb0c9-129">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cb0c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0c9-130">CommonParameters</span></span>
<span data-ttu-id="cb0c9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0c9-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0c9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0c9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb0c9-133">INPUTS</span></span>

## <span data-ttu-id="cb0c9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb0c9-134">OUTPUTS</span></span>

### <span data-ttu-id="cb0c9-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="cb0c9-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="cb0c9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb0c9-136">NOTES</span></span>

## <span data-ttu-id="cb0c9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb0c9-137">RELATED LINKS</span></span>

