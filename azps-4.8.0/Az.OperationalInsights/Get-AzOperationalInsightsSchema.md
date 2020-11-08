---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114735"
---
# <span data-ttu-id="ecad9-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="ecad9-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="ecad9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecad9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecad9-103">Retorna o esquema associado a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecad9-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="ecad9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecad9-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecad9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecad9-105">DESCRIPTION</span></span>
<span data-ttu-id="ecad9-106">O cmdlet **Get-AzOperationalInsightsSchema** retorna o esquema associado ao espaço de trabalho especificado dentro desse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ecad9-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="ecad9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecad9-107">EXAMPLES</span></span>

### <span data-ttu-id="ecad9-108">Exemplo 1: obter os esquemas de um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ecad9-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ecad9-109">Esse comando obtém os esquemas associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecad9-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="ecad9-110">OS</span><span class="sxs-lookup"><span data-stu-id="ecad9-110">PARAMETERS</span></span>

### <span data-ttu-id="ecad9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecad9-111">-DefaultProfile</span></span>
<span data-ttu-id="ecad9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ecad9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecad9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecad9-113">-ResourceGroupName</span></span>
<span data-ttu-id="ecad9-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecad9-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ecad9-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ecad9-115">-WorkspaceName</span></span>
<span data-ttu-id="ecad9-116">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecad9-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="ecad9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecad9-117">CommonParameters</span></span>
<span data-ttu-id="ecad9-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecad9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecad9-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecad9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecad9-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecad9-120">INPUTS</span></span>

### <span data-ttu-id="ecad9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ecad9-121">System.String</span></span>

## <span data-ttu-id="ecad9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecad9-122">OUTPUTS</span></span>

### <span data-ttu-id="ecad9-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="ecad9-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="ecad9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecad9-124">NOTES</span></span>

## <span data-ttu-id="ecad9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecad9-125">RELATED LINKS</span></span>

[<span data-ttu-id="ecad9-126">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="ecad9-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


