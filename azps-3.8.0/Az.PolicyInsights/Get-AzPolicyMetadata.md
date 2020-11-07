---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944472"
---
# <span data-ttu-id="2a453-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="2a453-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="2a453-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a453-102">SYNOPSIS</span></span>
<span data-ttu-id="2a453-103">Obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="2a453-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="2a453-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a453-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a453-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a453-105">DESCRIPTION</span></span>
<span data-ttu-id="2a453-106">O cmdlet **Get-AzPolicyRemediation** Obtém todos os recursos de metadados de política ou um recurso de metadados de política específico.</span><span class="sxs-lookup"><span data-stu-id="2a453-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="2a453-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a453-107">EXAMPLES</span></span>

### <span data-ttu-id="2a453-108">Exemplo 1: obter todos os recursos de metadados da política</span><span class="sxs-lookup"><span data-stu-id="2a453-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="2a453-109">Este comando obtém todos os recursos de metadados da política</span><span class="sxs-lookup"><span data-stu-id="2a453-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="2a453-110">Exemplo 2: obter um conjunto de 10 recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="2a453-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="2a453-111">Esse comando obtém uma coleção de 10 recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="2a453-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="2a453-112">Exemplo 3: obter um único recurso de metadados de política com o nome "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="2a453-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="2a453-113">Esse comando obtém um único recurso de metadados de política com o nome "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="2a453-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="2a453-114">OS</span><span class="sxs-lookup"><span data-stu-id="2a453-114">PARAMETERS</span></span>

### <span data-ttu-id="2a453-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a453-115">-DefaultProfile</span></span>
<span data-ttu-id="2a453-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a453-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a453-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a453-117">-Name</span></span>
<span data-ttu-id="2a453-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a453-118">Resource name.</span></span>

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

### <span data-ttu-id="2a453-119">-Início</span><span class="sxs-lookup"><span data-stu-id="2a453-119">-Top</span></span>
<span data-ttu-id="2a453-120">Número máximo de recursos de metadados de política a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="2a453-120">Maximum number of policy metadata resources to return.</span></span>

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

### <span data-ttu-id="2a453-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a453-121">CommonParameters</span></span>
<span data-ttu-id="2a453-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a453-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a453-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a453-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a453-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a453-124">INPUTS</span></span>

### <span data-ttu-id="2a453-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2a453-125">System.String</span></span>

## <span data-ttu-id="2a453-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a453-126">OUTPUTS</span></span>

### <span data-ttu-id="2a453-127">Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="2a453-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="2a453-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a453-128">NOTES</span></span>

## <span data-ttu-id="2a453-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a453-129">RELATED LINKS</span></span>
