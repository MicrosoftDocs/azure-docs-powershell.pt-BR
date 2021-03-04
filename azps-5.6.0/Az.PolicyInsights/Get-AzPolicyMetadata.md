---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: 85a5c38038116d89e7cab1e6efe2718d4c5a697b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890115"
---
# <span data-ttu-id="5d073-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="5d073-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="5d073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d073-102">SYNOPSIS</span></span>
<span data-ttu-id="5d073-103">Obtém recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5d073-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="5d073-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5d073-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d073-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5d073-105">DESCRIPTION</span></span>
<span data-ttu-id="5d073-106">O cmdlet **Get-AzPolicyRemediation** obtém todos os recursos de metadados de política ou um determinado recurso de metadados de política.</span><span class="sxs-lookup"><span data-stu-id="5d073-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="5d073-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d073-107">EXAMPLES</span></span>

### <span data-ttu-id="5d073-108">Exemplo 1: Obter todos os recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5d073-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="5d073-109">Este comando obtém todos os recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5d073-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="5d073-110">Exemplo 2: Obter uma coleção de 10 recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5d073-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="5d073-111">Este comando obtém uma coleção de 10 recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5d073-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="5d073-112">Exemplo 3: Obter um único recurso de metadados de política com o nome 'ACF1348'</span><span class="sxs-lookup"><span data-stu-id="5d073-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="5d073-113">Este comando obtém um único recurso de metadados de política com o nome 'ACF1348'</span><span class="sxs-lookup"><span data-stu-id="5d073-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="5d073-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5d073-114">PARAMETERS</span></span>

### <span data-ttu-id="5d073-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d073-115">-DefaultProfile</span></span>
<span data-ttu-id="5d073-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d073-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d073-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5d073-117">-Name</span></span>
<span data-ttu-id="5d073-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5d073-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d073-119">-Top</span><span class="sxs-lookup"><span data-stu-id="5d073-119">-Top</span></span>
<span data-ttu-id="5d073-120">Número máximo de recursos de metadados de política a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="5d073-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d073-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d073-121">CommonParameters</span></span>
<span data-ttu-id="5d073-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d073-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d073-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d073-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d073-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d073-124">INPUTS</span></span>

### <span data-ttu-id="5d073-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5d073-125">System.String</span></span>

## <span data-ttu-id="5d073-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5d073-126">OUTPUTS</span></span>

### <span data-ttu-id="5d073-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="5d073-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="5d073-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="5d073-128">NOTES</span></span>

## <span data-ttu-id="5d073-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d073-129">RELATED LINKS</span></span>
