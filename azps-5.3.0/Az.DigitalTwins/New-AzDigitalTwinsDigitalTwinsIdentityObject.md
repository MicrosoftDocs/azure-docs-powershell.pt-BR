---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428351"
---
# <span data-ttu-id="7f317-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="7f317-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="7f317-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f317-102">SYNOPSIS</span></span>
<span data-ttu-id="7f317-103">Criar um objeto de memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7f317-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7f317-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f317-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f317-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f317-105">DESCRIPTION</span></span>
<span data-ttu-id="7f317-106">Criar um objeto de memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7f317-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7f317-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f317-107">EXAMPLES</span></span>

### <span data-ttu-id="7f317-108">Exemplo 1: criar um DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="7f317-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="7f317-109">Criar um DigitalTwinsIdentityObject por ID e local</span><span class="sxs-lookup"><span data-stu-id="7f317-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="7f317-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f317-110">PARAMETERS</span></span>

### <span data-ttu-id="7f317-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f317-111">-EndpointName</span></span>
<span data-ttu-id="7f317-112">Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="7f317-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="7f317-113">-ID</span><span class="sxs-lookup"><span data-stu-id="7f317-113">-Id</span></span>
<span data-ttu-id="7f317-114">Caminho de identidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f317-114">Resource identity path.</span></span>

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

### <span data-ttu-id="7f317-115">-Local</span><span class="sxs-lookup"><span data-stu-id="7f317-115">-Location</span></span>
<span data-ttu-id="7f317-116">Local do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7f317-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7f317-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f317-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f317-118">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7f317-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7f317-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7f317-119">-ResourceName</span></span>
<span data-ttu-id="7f317-120">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="7f317-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="7f317-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f317-121">-SubscriptionId</span></span>
<span data-ttu-id="7f317-122">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="7f317-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="7f317-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f317-123">CommonParameters</span></span>
<span data-ttu-id="7f317-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f317-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f317-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f317-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f317-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f317-126">INPUTS</span></span>

## <span data-ttu-id="7f317-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f317-127">OUTPUTS</span></span>

### <span data-ttu-id="7f317-128">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="7f317-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="7f317-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f317-129">NOTES</span></span>

<span data-ttu-id="7f317-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7f317-130">ALIASES</span></span>

## <span data-ttu-id="7f317-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f317-131">RELATED LINKS</span></span>

