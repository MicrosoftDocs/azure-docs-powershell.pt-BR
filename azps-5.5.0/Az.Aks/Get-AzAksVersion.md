---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116683"
---
# <span data-ttu-id="06820-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="06820-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="06820-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06820-102">SYNOPSIS</span></span>
<span data-ttu-id="06820-103">Lista de versões disponíveis para a criação de cluster de Listernetes gerenciados.</span><span class="sxs-lookup"><span data-stu-id="06820-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="06820-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06820-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06820-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="06820-105">DESCRIPTION</span></span>
<span data-ttu-id="06820-106">Lista de versão disponível para a criação de cluster de Listagem gerenciada.</span><span class="sxs-lookup"><span data-stu-id="06820-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="06820-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06820-107">EXAMPLES</span></span>

### <span data-ttu-id="06820-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06820-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="06820-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06820-109">PARAMETERS</span></span>

### <span data-ttu-id="06820-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06820-110">-DefaultProfile</span></span>
<span data-ttu-id="06820-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06820-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06820-112">-Local</span><span class="sxs-lookup"><span data-stu-id="06820-112">-Location</span></span>
<span data-ttu-id="06820-113">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="06820-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="06820-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06820-114">CommonParameters</span></span>
<span data-ttu-id="06820-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06820-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06820-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06820-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06820-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="06820-117">INPUTS</span></span>

### <span data-ttu-id="06820-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06820-118">None</span></span>

## <span data-ttu-id="06820-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="06820-119">OUTPUTS</span></span>

### <span data-ttu-id="06820-120">Microsoft.Azure.Commands.Aks.Models.PSOfiletratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="06820-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="06820-121">Notas</span><span class="sxs-lookup"><span data-stu-id="06820-121">NOTES</span></span>

## <span data-ttu-id="06820-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06820-122">RELATED LINKS</span></span>
