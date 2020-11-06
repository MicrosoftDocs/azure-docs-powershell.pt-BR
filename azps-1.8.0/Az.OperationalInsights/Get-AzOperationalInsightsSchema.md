---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601936"
---
# <span data-ttu-id="f9847-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="f9847-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="f9847-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9847-102">SYNOPSIS</span></span>
<span data-ttu-id="f9847-103">Retorna o esquema associado a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9847-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="f9847-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9847-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9847-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9847-105">DESCRIPTION</span></span>
<span data-ttu-id="f9847-106">O cmdlet **Get-AzOperationalInsightsSchema** retorna o esquema associado ao espaço de trabalho especificado dentro desse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9847-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="f9847-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9847-107">EXAMPLES</span></span>

### <span data-ttu-id="f9847-108">Exemplo 1: obter os esquemas de um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="f9847-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="f9847-109">Esse comando obtém os esquemas associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9847-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="f9847-110">OS</span><span class="sxs-lookup"><span data-stu-id="f9847-110">PARAMETERS</span></span>

### <span data-ttu-id="f9847-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9847-111">-DefaultProfile</span></span>
<span data-ttu-id="f9847-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f9847-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9847-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9847-113">-ResourceGroupName</span></span>
<span data-ttu-id="f9847-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9847-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="f9847-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9847-115">-WorkspaceName</span></span>
<span data-ttu-id="f9847-116">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9847-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="f9847-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9847-117">CommonParameters</span></span>
<span data-ttu-id="f9847-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9847-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9847-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9847-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9847-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9847-120">INPUTS</span></span>

### <span data-ttu-id="f9847-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f9847-121">System.String</span></span>

## <span data-ttu-id="f9847-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9847-122">OUTPUTS</span></span>

### <span data-ttu-id="f9847-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="f9847-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="f9847-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9847-124">NOTES</span></span>

## <span data-ttu-id="f9847-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9847-125">RELATED LINKS</span></span>

[<span data-ttu-id="f9847-126">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="f9847-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


