---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774781"
---
# <span data-ttu-id="41250-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="41250-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="41250-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41250-102">SYNOPSIS</span></span>
<span data-ttu-id="41250-103">Lista todos os locatários de diretório na assinatura atual e o nome do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="41250-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="41250-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41250-104">SYNTAX</span></span>

### <span data-ttu-id="41250-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="41250-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="41250-106">Obter</span><span class="sxs-lookup"><span data-stu-id="41250-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="41250-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="41250-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="41250-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41250-108">DESCRIPTION</span></span>
<span data-ttu-id="41250-109">Lista todos os locatários de diretório na assinatura atual e o nome do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="41250-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="41250-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41250-110">EXAMPLES</span></span>

### <span data-ttu-id="41250-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41250-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="41250-112">Lista todos os locatários de diretório na assinatura atual e o nome do grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="41250-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="41250-113">OS</span><span class="sxs-lookup"><span data-stu-id="41250-113">PARAMETERS</span></span>

### <span data-ttu-id="41250-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="41250-114">-Name</span></span>
<span data-ttu-id="41250-115">Nome do locatário de diretório.</span><span class="sxs-lookup"><span data-stu-id="41250-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="41250-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41250-116">-ResourceGroupName</span></span>
<span data-ttu-id="41250-117">{{Fill ResourceGroupName descrição}}</span><span class="sxs-lookup"><span data-stu-id="41250-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="41250-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41250-118">-ResourceId</span></span>
<span data-ttu-id="41250-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="41250-119">The resource id.</span></span>

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

### <span data-ttu-id="41250-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="41250-120">-Skip</span></span>
<span data-ttu-id="41250-121">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="41250-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="41250-122">-Início</span><span class="sxs-lookup"><span data-stu-id="41250-122">-Top</span></span>
<span data-ttu-id="41250-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="41250-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="41250-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="41250-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="41250-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41250-125">CommonParameters</span></span>
<span data-ttu-id="41250-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41250-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41250-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41250-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41250-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41250-128">INPUTS</span></span>

## <span data-ttu-id="41250-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41250-129">OUTPUTS</span></span>

### <span data-ttu-id="41250-130">Microsoft. AzureStack. Management. subscriptions. admin. Models. DirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="41250-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="41250-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41250-131">NOTES</span></span>

## <span data-ttu-id="41250-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41250-132">RELATED LINKS</span></span>

