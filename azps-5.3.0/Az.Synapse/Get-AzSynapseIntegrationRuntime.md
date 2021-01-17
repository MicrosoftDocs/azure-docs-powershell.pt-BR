---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427613"
---
# <span data-ttu-id="81d11-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="81d11-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="81d11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81d11-102">SYNOPSIS</span></span>
<span data-ttu-id="81d11-103">Obtém informações sobre os recursos do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="81d11-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="81d11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81d11-104">SYNTAX</span></span>

### <span data-ttu-id="81d11-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="81d11-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81d11-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d11-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81d11-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d11-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81d11-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d11-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d11-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81d11-109">DESCRIPTION</span></span>
<span data-ttu-id="81d11-110">O cmdlet **Get-AzSynapseIntegrationRuntime** Obtém informações sobre os tempos de execução de integração em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81d11-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="81d11-111">Se você especificar o nome de um tempo de execução de integração, esse cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="81d11-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="81d11-112">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81d11-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="81d11-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81d11-113">EXAMPLES</span></span>

### <span data-ttu-id="81d11-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81d11-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="81d11-115">Liste todos os tempos de execução de integração no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81d11-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="81d11-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81d11-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="81d11-117">Esse comando exibe informações sobre o tempo de execução de integração chamado "Test-selfhost-IV" no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81d11-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="81d11-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="81d11-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="81d11-119">Esse comando exibe o status detalhado sobre o tempo de execução de integração chamado "Test-selfhost-IV" no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81d11-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="81d11-120">OS</span><span class="sxs-lookup"><span data-stu-id="81d11-120">PARAMETERS</span></span>

### <span data-ttu-id="81d11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d11-121">-DefaultProfile</span></span>
<span data-ttu-id="81d11-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81d11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d11-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81d11-123">-InputObject</span></span>
<span data-ttu-id="81d11-124">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="81d11-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d11-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="81d11-125">-Name</span></span>
<span data-ttu-id="81d11-126">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="81d11-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d11-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d11-127">-ResourceGroupName</span></span>
<span data-ttu-id="81d11-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81d11-128">Resource group name.</span></span>

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

### <span data-ttu-id="81d11-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d11-129">-ResourceId</span></span>
<span data-ttu-id="81d11-130">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="81d11-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d11-131">-Status</span><span class="sxs-lookup"><span data-stu-id="81d11-131">-Status</span></span>
<span data-ttu-id="81d11-132">O status do detalhe do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="81d11-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="81d11-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81d11-133">-WorkspaceName</span></span>
<span data-ttu-id="81d11-134">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="81d11-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="81d11-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="81d11-135">-WorkspaceObject</span></span>
<span data-ttu-id="81d11-136">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="81d11-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="81d11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d11-137">CommonParameters</span></span>
<span data-ttu-id="81d11-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d11-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d11-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d11-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81d11-140">INPUTS</span></span>

### <span data-ttu-id="81d11-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="81d11-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="81d11-142">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="81d11-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="81d11-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81d11-143">OUTPUTS</span></span>

### <span data-ttu-id="81d11-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="81d11-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="81d11-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81d11-145">NOTES</span></span>

## <span data-ttu-id="81d11-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81d11-146">RELATED LINKS</span></span>
