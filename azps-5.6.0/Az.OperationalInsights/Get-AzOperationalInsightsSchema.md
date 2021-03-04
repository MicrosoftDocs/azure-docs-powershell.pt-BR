---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 7f177b94b851f1a3702a153032c715f81badbcc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892737"
---
# <span data-ttu-id="5e3d2-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="5e3d2-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="5e3d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3d2-103">Retorna o esquema associado a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="5e3d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5e3d2-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e3d2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5e3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="5e3d2-106">O cmdlet **Get-AzOperationalInsightsSchema** retorna o esquema associado ao espaço de trabalho especificado nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="5e3d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="5e3d2-108">Exemplo 1: Obter os esquemas para um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5e3d2-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="5e3d2-109">Este comando obtém os esquemas associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="5e3d2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-110">PARAMETERS</span></span>

### <span data-ttu-id="5e3d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e3d2-111">-DefaultProfile</span></span>
<span data-ttu-id="5e3d2-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5e3d2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e3d2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e3d2-113">-ResourceGroupName</span></span>
<span data-ttu-id="5e3d2-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3d2-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5e3d2-115">-WorkspaceName</span></span>
<span data-ttu-id="5e3d2-116">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3d2-117">CommonParameters</span></span>
<span data-ttu-id="5e3d2-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e3d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3d2-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e3d2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3d2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-120">INPUTS</span></span>

### <span data-ttu-id="5e3d2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5e3d2-121">System.String</span></span>

## <span data-ttu-id="5e3d2-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-122">OUTPUTS</span></span>

### <span data-ttu-id="5e3d2-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="5e3d2-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="5e3d2-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="5e3d2-124">NOTES</span></span>

## <span data-ttu-id="5e3d2-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e3d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e3d2-126">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="5e3d2-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


