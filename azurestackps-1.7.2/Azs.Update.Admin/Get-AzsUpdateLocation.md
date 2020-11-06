---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595631"
---
# <span data-ttu-id="39f20-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="39f20-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="39f20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39f20-102">SYNOPSIS</span></span>
<span data-ttu-id="39f20-103">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="39f20-103">Get the list of update locations.</span></span>

## <span data-ttu-id="39f20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39f20-104">SYNTAX</span></span>

### <span data-ttu-id="39f20-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="39f20-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="39f20-106">Obter</span><span class="sxs-lookup"><span data-stu-id="39f20-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="39f20-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="39f20-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="39f20-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39f20-108">DESCRIPTION</span></span>
<span data-ttu-id="39f20-109">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="39f20-109">Get the list of update locations.</span></span> <span data-ttu-id="39f20-110">Os locais retornados podem ser usados para obter as atualizações disponíveis em um local específico usando Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="39f20-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="39f20-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39f20-111">EXAMPLES</span></span>

### <span data-ttu-id="39f20-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="39f20-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="39f20-113">Obter a lista de locais de atualização.</span><span class="sxs-lookup"><span data-stu-id="39f20-113">Get the list of update locations.</span></span>

## <span data-ttu-id="39f20-114">OS</span><span class="sxs-lookup"><span data-stu-id="39f20-114">PARAMETERS</span></span>

### <span data-ttu-id="39f20-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="39f20-115">-Name</span></span>
<span data-ttu-id="39f20-116">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="39f20-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f20-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f20-117">-ResourceGroupName</span></span>
<span data-ttu-id="39f20-118">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="39f20-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="39f20-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f20-119">-ResourceId</span></span>
<span data-ttu-id="39f20-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="39f20-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f20-121">CommonParameters</span></span>
<span data-ttu-id="39f20-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f20-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f20-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f20-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39f20-124">INPUTS</span></span>

## <span data-ttu-id="39f20-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39f20-125">OUTPUTS</span></span>

### <span data-ttu-id="39f20-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="39f20-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="39f20-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39f20-127">NOTES</span></span>

## <span data-ttu-id="39f20-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39f20-128">RELATED LINKS</span></span>

