---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: 50d4dc8531f28ebb50ef562321b3974c7b50a102
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887253"
---
# <span data-ttu-id="59a6b-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="59a6b-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="59a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="59a6b-103">Listar clusters gerenciados kubernetes.</span><span class="sxs-lookup"><span data-stu-id="59a6b-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="59a6b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="59a6b-104">SYNTAX</span></span>

### <span data-ttu-id="59a6b-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="59a6b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59a6b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a6b-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59a6b-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59a6b-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a6b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="59a6b-108">DESCRIPTION</span></span>
<span data-ttu-id="59a6b-109">Listar clusters gerenciados kubernetes.</span><span class="sxs-lookup"><span data-stu-id="59a6b-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="59a6b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59a6b-110">EXAMPLES</span></span>

### <span data-ttu-id="59a6b-111">Listar todos os clusters kubernetes</span><span class="sxs-lookup"><span data-stu-id="59a6b-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="59a6b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="59a6b-112">PARAMETERS</span></span>

### <span data-ttu-id="59a6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a6b-113">-DefaultProfile</span></span>
<span data-ttu-id="59a6b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59a6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a6b-115">-Id</span><span class="sxs-lookup"><span data-stu-id="59a6b-115">-Id</span></span>
<span data-ttu-id="59a6b-116">ID de um cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="59a6b-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59a6b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="59a6b-117">-Name</span></span>
<span data-ttu-id="59a6b-118">Nome do cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="59a6b-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="59a6b-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="59a6b-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a6b-121">CommonParameters</span></span>
<span data-ttu-id="59a6b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a6b-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59a6b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a6b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59a6b-124">INPUTS</span></span>

### <span data-ttu-id="59a6b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="59a6b-125">System.String</span></span>

## <span data-ttu-id="59a6b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="59a6b-126">OUTPUTS</span></span>

### <span data-ttu-id="59a6b-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="59a6b-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="59a6b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="59a6b-128">NOTES</span></span>

## <span data-ttu-id="59a6b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59a6b-129">RELATED LINKS</span></span>
