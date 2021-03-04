---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: 2b038699dfa1cd959ea20b761b6c24dee69a9e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889517"
---
# <span data-ttu-id="d4615-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="d4615-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="d4615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4615-102">SYNOPSIS</span></span>
<span data-ttu-id="d4615-103">Criar um objeto na memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d4615-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d4615-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4615-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4615-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4615-105">DESCRIPTION</span></span>
<span data-ttu-id="d4615-106">Criar um objeto na memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d4615-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d4615-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4615-107">EXAMPLES</span></span>

### <span data-ttu-id="d4615-108">Exemplo 1: Criar um DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="d4615-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="d4615-109">Criar Um DigitalTwinsIdentityObject por ID e local</span><span class="sxs-lookup"><span data-stu-id="d4615-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="d4615-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4615-110">PARAMETERS</span></span>

### <span data-ttu-id="d4615-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d4615-111">-EndpointName</span></span>
<span data-ttu-id="d4615-112">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="d4615-112">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-113">-Id</span><span class="sxs-lookup"><span data-stu-id="d4615-113">-Id</span></span>
<span data-ttu-id="d4615-114">Caminho da identidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="d4615-114">Resource identity path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d4615-115">-Location</span></span>
<span data-ttu-id="d4615-116">Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d4615-116">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4615-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4615-118">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d4615-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d4615-119">-ResourceName</span></span>
<span data-ttu-id="d4615-120">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="d4615-120">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4615-121">-SubscriptionId</span></span>
<span data-ttu-id="d4615-122">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4615-122">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4615-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4615-123">CommonParameters</span></span>
<span data-ttu-id="d4615-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4615-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4615-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4615-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4615-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4615-126">INPUTS</span></span>

## <span data-ttu-id="d4615-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4615-127">OUTPUTS</span></span>

### <span data-ttu-id="d4615-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="d4615-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="d4615-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4615-129">NOTES</span></span>

<span data-ttu-id="d4615-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d4615-130">ALIASES</span></span>

## <span data-ttu-id="d4615-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4615-131">RELATED LINKS</span></span>

