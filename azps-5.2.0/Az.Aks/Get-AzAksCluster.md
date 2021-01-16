---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259791"
---
# <span data-ttu-id="ed910-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="ed910-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="ed910-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed910-102">SYNOPSIS</span></span>
<span data-ttu-id="ed910-103">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ed910-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="ed910-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed910-104">SYNTAX</span></span>

### <span data-ttu-id="ed910-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed910-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed910-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed910-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed910-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed910-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed910-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed910-108">DESCRIPTION</span></span>
<span data-ttu-id="ed910-109">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ed910-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="ed910-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed910-110">EXAMPLES</span></span>

### <span data-ttu-id="ed910-111">Listar todos os clusters do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed910-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="ed910-112">OS</span><span class="sxs-lookup"><span data-stu-id="ed910-112">PARAMETERS</span></span>

### <span data-ttu-id="ed910-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed910-113">-DefaultProfile</span></span>
<span data-ttu-id="ed910-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed910-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed910-115">-ID</span><span class="sxs-lookup"><span data-stu-id="ed910-115">-Id</span></span>
<span data-ttu-id="ed910-116">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed910-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ed910-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed910-117">-Name</span></span>
<span data-ttu-id="ed910-118">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ed910-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ed910-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed910-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed910-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed910-120">Resource group name</span></span>

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

### <span data-ttu-id="ed910-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed910-121">CommonParameters</span></span>
<span data-ttu-id="ed910-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed910-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed910-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed910-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed910-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed910-124">INPUTS</span></span>

### <span data-ttu-id="ed910-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ed910-125">System.String</span></span>

## <span data-ttu-id="ed910-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed910-126">OUTPUTS</span></span>

### <span data-ttu-id="ed910-127">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ed910-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ed910-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed910-128">NOTES</span></span>

## <span data-ttu-id="ed910-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed910-129">RELATED LINKS</span></span>
