---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112417"
---
# <span data-ttu-id="3e16a-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3e16a-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="3e16a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e16a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e16a-103">Obtém chaves para um tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="3e16a-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="3e16a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e16a-104">SYNTAX</span></span>

### <span data-ttu-id="3e16a-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e16a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e16a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e16a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e16a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e16a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e16a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e16a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e16a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e16a-109">DESCRIPTION</span></span>
<span data-ttu-id="3e16a-110">O cmdlet **Get-AzSynapseIntegrationRuntimeKey** obtém chaves para um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e16a-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="3e16a-111">As teclas são usadas para registrar um nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e16a-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="3e16a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e16a-112">EXAMPLES</span></span>

### <span data-ttu-id="3e16a-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e16a-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="3e16a-114">O cmdlet recupera chaves para um tempo de execução de integração chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="3e16a-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3e16a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e16a-115">PARAMETERS</span></span>

### <span data-ttu-id="3e16a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e16a-116">-DefaultProfile</span></span>
<span data-ttu-id="3e16a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e16a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e16a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e16a-118">-InputObject</span></span>
<span data-ttu-id="3e16a-119">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e16a-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="3e16a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e16a-120">-Name</span></span>
<span data-ttu-id="3e16a-121">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="3e16a-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e16a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e16a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e16a-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e16a-123">Resource group name.</span></span>

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

### <span data-ttu-id="3e16a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e16a-124">-ResourceId</span></span>
<span data-ttu-id="3e16a-125">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="3e16a-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3e16a-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="3e16a-126">-WorkspaceName</span></span>
<span data-ttu-id="3e16a-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e16a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e16a-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e16a-128">-WorkspaceObject</span></span>
<span data-ttu-id="3e16a-129">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e16a-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e16a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e16a-130">CommonParameters</span></span>
<span data-ttu-id="3e16a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e16a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e16a-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e16a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e16a-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e16a-133">INPUTS</span></span>

### <span data-ttu-id="3e16a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e16a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3e16a-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e16a-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3e16a-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e16a-136">OUTPUTS</span></span>

### <span data-ttu-id="3e16a-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="3e16a-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="3e16a-138">Notas</span><span class="sxs-lookup"><span data-stu-id="3e16a-138">NOTES</span></span>

## <span data-ttu-id="3e16a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e16a-139">RELATED LINKS</span></span>
