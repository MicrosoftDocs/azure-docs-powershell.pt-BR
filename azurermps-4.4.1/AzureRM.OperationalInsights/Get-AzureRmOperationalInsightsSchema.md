---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: a4e4f1d86822a6c4ecd793576b1a5b68f2b2534f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430703"
---
# <span data-ttu-id="06767-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="06767-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="06767-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06767-102">SYNOPSIS</span></span>
<span data-ttu-id="06767-103">Retorna o esquema associado a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06767-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06767-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06767-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06767-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06767-105">DESCRIPTION</span></span>
<span data-ttu-id="06767-106">O cmdlet **Get-AzureRmOperationalInsightsSchema** retorna o esquema associado ao espaço de trabalho especificado dentro desse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06767-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="06767-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06767-107">EXAMPLES</span></span>

### <span data-ttu-id="06767-108">Exemplo 1: obter os esquemas de um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="06767-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="06767-109">Esse comando obtém os esquemas associados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06767-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="06767-110">OS</span><span class="sxs-lookup"><span data-stu-id="06767-110">PARAMETERS</span></span>

### <span data-ttu-id="06767-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06767-111">-ResourceGroupName</span></span>
<span data-ttu-id="06767-112">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06767-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="06767-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06767-113">-WorkspaceName</span></span>
<span data-ttu-id="06767-114">Especifica um nome de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06767-114">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="06767-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06767-115">-DefaultProfile</span></span>
<span data-ttu-id="06767-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06767-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06767-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06767-117">CommonParameters</span></span>
<span data-ttu-id="06767-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06767-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06767-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06767-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06767-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06767-120">INPUTS</span></span>

## <span data-ttu-id="06767-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06767-121">OUTPUTS</span></span>

### <span data-ttu-id="06767-122">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="06767-122">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="06767-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06767-123">NOTES</span></span>

## <span data-ttu-id="06767-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06767-124">RELATED LINKS</span></span>

[<span data-ttu-id="06767-125">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="06767-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

