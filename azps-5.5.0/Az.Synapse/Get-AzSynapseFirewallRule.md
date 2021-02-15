---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118898"
---
# <span data-ttu-id="c9aa3-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9aa3-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="c9aa3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="c9aa3-103">Obtém uma Regra de Firewall de Análise Synapse.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="c9aa3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9aa3-104">SYNTAX</span></span>

### <span data-ttu-id="c9aa3-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c9aa3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9aa3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9aa3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9aa3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="c9aa3-108">O cmdlet **Get-AzSynapseFirewallRule** obtém uma Regra de Firewall do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="c9aa3-109">Se você não especificar um nome de regra, esse cmdlet obtém todas as regras.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="c9aa3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9aa3-110">EXAMPLES</span></span>

### <span data-ttu-id="c9aa3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9aa3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c9aa3-112">Esse comando obtém todas as regras de firewall em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="c9aa3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c9aa3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="c9aa3-114">Esse comando obtém a regra de firewall no espaço de trabalho ContosoWorkspace com o nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="c9aa3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c9aa3-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="c9aa3-116">Esse comando obtém todas as regras de firewall em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="c9aa3-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9aa3-117">PARAMETERS</span></span>

### <span data-ttu-id="c9aa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9aa3-118">-DefaultProfile</span></span>
<span data-ttu-id="c9aa3-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9aa3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9aa3-120">-Name</span></span>
<span data-ttu-id="c9aa3-121">O nome da regra de firerwall para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9aa3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9aa3-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9aa3-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9aa3-124">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c9aa3-124">-WorkspaceName</span></span>
<span data-ttu-id="c9aa3-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9aa3-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="c9aa3-126">-WorkSpaceObject</span></span>
<span data-ttu-id="c9aa3-127">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9aa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9aa3-128">CommonParameters</span></span>
<span data-ttu-id="c9aa3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9aa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9aa3-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9aa3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9aa3-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9aa3-131">INPUTS</span></span>

### <span data-ttu-id="c9aa3-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9aa3-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c9aa3-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9aa3-133">OUTPUTS</span></span>

### <span data-ttu-id="c9aa3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9aa3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="c9aa3-135">Notas</span><span class="sxs-lookup"><span data-stu-id="c9aa3-135">NOTES</span></span>

## <span data-ttu-id="c9aa3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9aa3-136">RELATED LINKS</span></span>
