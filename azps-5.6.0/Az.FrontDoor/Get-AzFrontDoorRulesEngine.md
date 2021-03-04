---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890845"
---
# <span data-ttu-id="517f6-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="517f6-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="517f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="517f6-102">SYNOPSIS</span></span>
<span data-ttu-id="517f6-103">Obter configurações do Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="517f6-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="517f6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="517f6-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="517f6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="517f6-105">DESCRIPTION</span></span>
<span data-ttu-id="517f6-106">O cmdlet **Get-AzFrontDoorRulesEngine** obtém uma configuração específica do mecanismo de regras ou obtém todas as configurações do mecanismo de regras associadas a uma Porta Da Frente.</span><span class="sxs-lookup"><span data-stu-id="517f6-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="517f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="517f6-107">EXAMPLES</span></span>

### <span data-ttu-id="517f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="517f6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="517f6-109">Obter configuração específica do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="517f6-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="517f6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="517f6-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="517f6-111">Obter todas as configurações do mecanismo de regras em uma porta da frente.</span><span class="sxs-lookup"><span data-stu-id="517f6-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="517f6-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="517f6-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="517f6-113">Saída esperada ao obter um mecanismo de regras inexistente.</span><span class="sxs-lookup"><span data-stu-id="517f6-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="517f6-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="517f6-114">PARAMETERS</span></span>

### <span data-ttu-id="517f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517f6-115">-DefaultProfile</span></span>
<span data-ttu-id="517f6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="517f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517f6-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="517f6-117">-FrontDoorName</span></span>
<span data-ttu-id="517f6-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="517f6-118">Front Door name.</span></span>

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

### <span data-ttu-id="517f6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="517f6-119">-Name</span></span>
<span data-ttu-id="517f6-120">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="517f6-120">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="517f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="517f6-122">O nome do grupo de recursos em que a Porta da Frente será criada.</span><span class="sxs-lookup"><span data-stu-id="517f6-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="517f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517f6-123">CommonParameters</span></span>
<span data-ttu-id="517f6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517f6-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="517f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517f6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="517f6-126">INPUTS</span></span>

### <span data-ttu-id="517f6-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="517f6-127">None</span></span>

## <span data-ttu-id="517f6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="517f6-128">OUTPUTS</span></span>

### <span data-ttu-id="517f6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="517f6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="517f6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="517f6-130">NOTES</span></span>

## <span data-ttu-id="517f6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="517f6-131">RELATED LINKS</span></span>
