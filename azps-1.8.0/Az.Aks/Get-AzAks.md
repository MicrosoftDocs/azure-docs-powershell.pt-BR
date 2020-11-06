---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595755"
---
# <span data-ttu-id="c377b-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="c377b-101">Get-AzAks</span></span>

## <span data-ttu-id="c377b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c377b-102">SYNOPSIS</span></span>
<span data-ttu-id="c377b-103">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c377b-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c377b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c377b-104">SYNTAX</span></span>

### <span data-ttu-id="c377b-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c377b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c377b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c377b-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c377b-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c377b-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c377b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c377b-108">DESCRIPTION</span></span>
<span data-ttu-id="c377b-109">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c377b-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c377b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c377b-110">EXAMPLES</span></span>

### <span data-ttu-id="c377b-111">Listar todos os clusters do kubernetes</span><span class="sxs-lookup"><span data-stu-id="c377b-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="c377b-112">OS</span><span class="sxs-lookup"><span data-stu-id="c377b-112">PARAMETERS</span></span>

### <span data-ttu-id="c377b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c377b-113">-DefaultProfile</span></span>
<span data-ttu-id="c377b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c377b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c377b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c377b-115">-Id</span></span>
<span data-ttu-id="c377b-116">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="c377b-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c377b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c377b-117">-Name</span></span>
<span data-ttu-id="c377b-118">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="c377b-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c377b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c377b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c377b-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c377b-120">Resource group name</span></span>

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

### <span data-ttu-id="c377b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c377b-121">CommonParameters</span></span>
<span data-ttu-id="c377b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c377b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c377b-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c377b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c377b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c377b-124">INPUTS</span></span>

### <span data-ttu-id="c377b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c377b-125">System.String</span></span>

## <span data-ttu-id="c377b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c377b-126">OUTPUTS</span></span>

### <span data-ttu-id="c377b-127">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c377b-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c377b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c377b-128">NOTES</span></span>

## <span data-ttu-id="c377b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c377b-129">RELATED LINKS</span></span>
