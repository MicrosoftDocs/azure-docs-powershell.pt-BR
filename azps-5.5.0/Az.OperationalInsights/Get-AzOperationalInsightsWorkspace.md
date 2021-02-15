---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111523"
---
# <span data-ttu-id="03b3f-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="03b3f-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="03b3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="03b3f-103">Obtém informações sobre um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="03b3f-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="03b3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03b3f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b3f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="03b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="03b3f-106">O cmdlet **Get-AzOperationalInsightsWorkspace** obtém informações sobre um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="03b3f-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="03b3f-107">Se você especificar um nome de espaço de trabalho, esse cmdlet obterá informações sobre esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="03b3f-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="03b3f-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os espaços de trabalho em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03b3f-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="03b3f-109">Se você não especificar um nome e um grupo de recursos, esse cmdlet obterá informações sobre todos os espaços de trabalho de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="03b3f-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="03b3f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03b3f-110">EXAMPLES</span></span>

### <span data-ttu-id="03b3f-111">Exemplo 1: Obter um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="03b3f-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="03b3f-112">Esse comando obtém um espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="03b3f-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="03b3f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03b3f-113">PARAMETERS</span></span>

### <span data-ttu-id="03b3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b3f-114">-DefaultProfile</span></span>
<span data-ttu-id="03b3f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="03b3f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03b3f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="03b3f-116">-Name</span></span>
<span data-ttu-id="03b3f-117">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="03b3f-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b3f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b3f-118">-ResourceGroupName</span></span>
<span data-ttu-id="03b3f-119">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="03b3f-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b3f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b3f-120">CommonParameters</span></span>
<span data-ttu-id="03b3f-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b3f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b3f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b3f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b3f-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="03b3f-123">INPUTS</span></span>

### <span data-ttu-id="03b3f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="03b3f-124">System.String</span></span>

## <span data-ttu-id="03b3f-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="03b3f-125">OUTPUTS</span></span>

### <span data-ttu-id="03b3f-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="03b3f-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="03b3f-127">Notas</span><span class="sxs-lookup"><span data-stu-id="03b3f-127">NOTES</span></span>

## <span data-ttu-id="03b3f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03b3f-128">RELATED LINKS</span></span>

[<span data-ttu-id="03b3f-129">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="03b3f-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


