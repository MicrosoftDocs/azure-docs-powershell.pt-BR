---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118531"
---
# <span data-ttu-id="c8f0b-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c8f0b-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="c8f0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f0b-103">Verifica a existência de um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="c8f0b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8f0b-104">SYNTAX</span></span>

### <span data-ttu-id="c8f0b-105">TestByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8f0b-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8f0b-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f0b-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8f0b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="c8f0b-108">O cmdlet **Test-AzSynapseSqlDatabase** verifica a existência de um banco de dados SQL do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="c8f0b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8f0b-109">EXAMPLES</span></span>

### <span data-ttu-id="c8f0b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8f0b-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="c8f0b-111">Esse comando verifica a existência do banco de dados SQL especificado.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="c8f0b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8f0b-112">PARAMETERS</span></span>

### <span data-ttu-id="c8f0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f0b-113">-DefaultProfile</span></span>
<span data-ttu-id="c8f0b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f0b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8f0b-115">-Name</span></span>
<span data-ttu-id="c8f0b-116">Nome do Banco de Dados SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="c8f0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8f0b-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0b-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c8f0b-119">-WorkspaceName</span></span>
<span data-ttu-id="c8f0b-120">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0b-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8f0b-121">-WorkspaceObject</span></span>
<span data-ttu-id="c8f0b-122">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f0b-123">CommonParameters</span></span>
<span data-ttu-id="c8f0b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f0b-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8f0b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f0b-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8f0b-126">INPUTS</span></span>

### <span data-ttu-id="c8f0b-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8f0b-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c8f0b-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8f0b-128">OUTPUTS</span></span>

### <span data-ttu-id="c8f0b-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8f0b-129">System.Boolean</span></span>

## <span data-ttu-id="c8f0b-130">Notas</span><span class="sxs-lookup"><span data-stu-id="c8f0b-130">NOTES</span></span>

## <span data-ttu-id="c8f0b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8f0b-131">RELATED LINKS</span></span>
