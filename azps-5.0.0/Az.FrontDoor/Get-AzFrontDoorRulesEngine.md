---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124999"
---
# <span data-ttu-id="49f59-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="49f59-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="49f59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49f59-102">SYNOPSIS</span></span>
<span data-ttu-id="49f59-103">Obter configurações do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="49f59-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="49f59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49f59-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49f59-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49f59-105">DESCRIPTION</span></span>
<span data-ttu-id="49f59-106">O cmdlet **Get-AzFrontDoorRulesEngine** Obtém uma configuração de mecanismo de regras específica ou obtém todas as configurações de mecanismo de regras associadas a uma porta frontal.</span><span class="sxs-lookup"><span data-stu-id="49f59-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="49f59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49f59-107">EXAMPLES</span></span>

### <span data-ttu-id="49f59-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="49f59-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="49f59-109">Obter configuração de mecanismo de regras específicas.</span><span class="sxs-lookup"><span data-stu-id="49f59-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="49f59-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="49f59-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="49f59-111">Obter todas as configurações do mecanismo de regras em uma porta frontal.</span><span class="sxs-lookup"><span data-stu-id="49f59-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="49f59-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="49f59-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="49f59-113">Saída esperada ao obter um mecanismo de regras inexistentes.</span><span class="sxs-lookup"><span data-stu-id="49f59-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="49f59-114">OS</span><span class="sxs-lookup"><span data-stu-id="49f59-114">PARAMETERS</span></span>

### <span data-ttu-id="49f59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f59-115">-DefaultProfile</span></span>
<span data-ttu-id="49f59-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49f59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f59-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="49f59-117">-FrontDoorName</span></span>
<span data-ttu-id="49f59-118">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="49f59-118">Front Door name.</span></span>

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

### <span data-ttu-id="49f59-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="49f59-119">-Name</span></span>
<span data-ttu-id="49f59-120">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="49f59-120">Rules engine name.</span></span>

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

### <span data-ttu-id="49f59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f59-121">-ResourceGroupName</span></span>
<span data-ttu-id="49f59-122">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="49f59-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="49f59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f59-123">CommonParameters</span></span>
<span data-ttu-id="49f59-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f59-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49f59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f59-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49f59-126">INPUTS</span></span>

### <span data-ttu-id="49f59-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="49f59-127">None</span></span>

## <span data-ttu-id="49f59-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49f59-128">OUTPUTS</span></span>

### <span data-ttu-id="49f59-129">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="49f59-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="49f59-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49f59-130">NOTES</span></span>

## <span data-ttu-id="49f59-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49f59-131">RELATED LINKS</span></span>
