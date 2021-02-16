---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126993"
---
# <span data-ttu-id="59c4a-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="59c4a-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="59c4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="59c4a-103">Criar um objeto na memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="59c4a-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="59c4a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59c4a-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="59c4a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="59c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="59c4a-106">Criar um objeto na memória para DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="59c4a-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="59c4a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="59c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="59c4a-108">Exemplo 1: Criar um DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="59c4a-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="59c4a-109">Criar Um DigitalTwinsIdentityObject por ID e local</span><span class="sxs-lookup"><span data-stu-id="59c4a-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="59c4a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59c4a-110">PARAMETERS</span></span>

### <span data-ttu-id="59c4a-111">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="59c4a-111">-EndpointName</span></span>
<span data-ttu-id="59c4a-112">Nome do Recurso de Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="59c4a-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="59c4a-113">-ID</span><span class="sxs-lookup"><span data-stu-id="59c4a-113">-Id</span></span>
<span data-ttu-id="59c4a-114">Caminho de identidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="59c4a-114">Resource identity path.</span></span>

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

### <span data-ttu-id="59c4a-115">-Local</span><span class="sxs-lookup"><span data-stu-id="59c4a-115">-Location</span></span>
<span data-ttu-id="59c4a-116">Local de DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="59c4a-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="59c4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="59c4a-118">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="59c4a-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="59c4a-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="59c4a-119">-ResourceName</span></span>
<span data-ttu-id="59c4a-120">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="59c4a-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="59c4a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59c4a-121">-SubscriptionId</span></span>
<span data-ttu-id="59c4a-122">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="59c4a-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="59c4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c4a-123">CommonParameters</span></span>
<span data-ttu-id="59c4a-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c4a-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59c4a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c4a-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="59c4a-126">INPUTS</span></span>

## <span data-ttu-id="59c4a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="59c4a-127">OUTPUTS</span></span>

### <span data-ttu-id="59c4a-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="59c4a-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="59c4a-129">Notas</span><span class="sxs-lookup"><span data-stu-id="59c4a-129">NOTES</span></span>

<span data-ttu-id="59c4a-130">Aliases</span><span class="sxs-lookup"><span data-stu-id="59c4a-130">ALIASES</span></span>

## <span data-ttu-id="59c4a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59c4a-131">RELATED LINKS</span></span>

