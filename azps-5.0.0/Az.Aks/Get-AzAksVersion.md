---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117115"
---
# <span data-ttu-id="c1797-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="c1797-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="c1797-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1797-102">SYNOPSIS</span></span>
<span data-ttu-id="c1797-103">Liste a versão disponível para a criação de um cluster gerenciado do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c1797-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c1797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1797-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1797-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1797-105">DESCRIPTION</span></span>
<span data-ttu-id="c1797-106">Liste a versão disponível para a criação de um cluster gerenciado do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c1797-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c1797-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1797-107">EXAMPLES</span></span>

### <span data-ttu-id="c1797-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1797-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="c1797-109">OS</span><span class="sxs-lookup"><span data-stu-id="c1797-109">PARAMETERS</span></span>

### <span data-ttu-id="c1797-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1797-110">-DefaultProfile</span></span>
<span data-ttu-id="c1797-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1797-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1797-112">-Local</span><span class="sxs-lookup"><span data-stu-id="c1797-112">-Location</span></span>
<span data-ttu-id="c1797-113">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c1797-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1797-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1797-114">CommonParameters</span></span>
<span data-ttu-id="c1797-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1797-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1797-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1797-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1797-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1797-117">INPUTS</span></span>

### <span data-ttu-id="c1797-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c1797-118">None</span></span>

## <span data-ttu-id="c1797-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1797-119">OUTPUTS</span></span>

### <span data-ttu-id="c1797-120">Microsoft. Azure. Commands. AKs. Models. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="c1797-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="c1797-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1797-121">NOTES</span></span>

## <span data-ttu-id="c1797-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1797-122">RELATED LINKS</span></span>
