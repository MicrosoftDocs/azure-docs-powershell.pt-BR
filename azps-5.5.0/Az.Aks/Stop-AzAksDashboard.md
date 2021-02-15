---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114877"
---
# <span data-ttu-id="c1b0d-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="c1b0d-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="c1b0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b0d-103">Pare o túnel SSH Descarreado criado no Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c1b0d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1b0d-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b0d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b0d-106">Pare o túnel SSH Descarreado criado no Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c1b0d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b0d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1b0d-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="c1b0d-109">Interrompe a configuração de túnel SSH existente executando Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="c1b0d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b0d-111">-DefaultProfile</span></span>
<span data-ttu-id="c1b0d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1b0d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1b0d-113">-PassThru</span></span>
<span data-ttu-id="c1b0d-114">Retorna verdadeiro se o túnel SSH estiver fechado.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="c1b0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b0d-115">CommonParameters</span></span>
<span data-ttu-id="c1b0d-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b0d-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1b0d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b0d-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1b0d-118">INPUTS</span></span>

### <span data-ttu-id="c1b0d-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1b0d-119">None</span></span>

## <span data-ttu-id="c1b0d-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1b0d-120">OUTPUTS</span></span>

### <span data-ttu-id="c1b0d-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b0d-121">System.Boolean</span></span>

## <span data-ttu-id="c1b0d-122">Notas</span><span class="sxs-lookup"><span data-stu-id="c1b0d-122">NOTES</span></span>

## <span data-ttu-id="c1b0d-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1b0d-123">RELATED LINKS</span></span>
