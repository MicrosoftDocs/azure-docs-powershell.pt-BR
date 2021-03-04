---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888340"
---
# <span data-ttu-id="6f242-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="6f242-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="6f242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f242-102">SYNOPSIS</span></span>
<span data-ttu-id="6f242-103">Pare o túnel SSH kubectl criado no Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6f242-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6f242-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f242-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f242-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f242-105">DESCRIPTION</span></span>
<span data-ttu-id="6f242-106">Pare o túnel SSH kubectl criado no Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6f242-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6f242-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f242-107">EXAMPLES</span></span>

### <span data-ttu-id="6f242-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f242-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="6f242-109">Interrompe a configuração de túnel SSH existente executando Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6f242-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6f242-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f242-110">PARAMETERS</span></span>

### <span data-ttu-id="6f242-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f242-111">-DefaultProfile</span></span>
<span data-ttu-id="6f242-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f242-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f242-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f242-113">-PassThru</span></span>
<span data-ttu-id="6f242-114">Retorna true se o túnel SSH estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="6f242-114">Returns true if SSH tunnel is closed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f242-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f242-115">CommonParameters</span></span>
<span data-ttu-id="6f242-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f242-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f242-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f242-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f242-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f242-118">INPUTS</span></span>

### <span data-ttu-id="6f242-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6f242-119">None</span></span>

## <span data-ttu-id="6f242-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f242-120">OUTPUTS</span></span>

### <span data-ttu-id="6f242-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f242-121">System.Boolean</span></span>

## <span data-ttu-id="6f242-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f242-122">NOTES</span></span>

## <span data-ttu-id="6f242-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f242-123">RELATED LINKS</span></span>
