---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887248"
---
# <span data-ttu-id="02ac1-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="02ac1-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="02ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="02ac1-103">Listar a versão disponível para a criação de cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="02ac1-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="02ac1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02ac1-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ac1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="02ac1-106">Listar a versão disponível para a criação de cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="02ac1-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="02ac1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="02ac1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02ac1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="02ac1-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02ac1-109">PARAMETERS</span></span>

### <span data-ttu-id="02ac1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ac1-110">-DefaultProfile</span></span>
<span data-ttu-id="02ac1-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02ac1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ac1-112">-Location</span><span class="sxs-lookup"><span data-stu-id="02ac1-112">-Location</span></span>
<span data-ttu-id="02ac1-113">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="02ac1-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="02ac1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ac1-114">CommonParameters</span></span>
<span data-ttu-id="02ac1-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ac1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ac1-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ac1-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ac1-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02ac1-117">INPUTS</span></span>

### <span data-ttu-id="02ac1-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="02ac1-118">None</span></span>

## <span data-ttu-id="02ac1-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02ac1-119">OUTPUTS</span></span>

### <span data-ttu-id="02ac1-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="02ac1-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="02ac1-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="02ac1-121">NOTES</span></span>

## <span data-ttu-id="02ac1-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02ac1-122">RELATED LINKS</span></span>
