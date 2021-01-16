---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272456"
---
# <span data-ttu-id="b2b25-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b2b25-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="b2b25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2b25-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b25-103">Desabilita a segurança avançada de dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2b25-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="b2b25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2b25-104">SYNTAX</span></span>

### <span data-ttu-id="b2b25-105">DisableByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2b25-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b25-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b25-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2b25-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b25-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b25-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2b25-108">DESCRIPTION</span></span>
<span data-ttu-id="b2b25-109">O cmdlet **Disable-AzSynapseSqlAdvancedDataSecurity** desabilita a segurança avançada de dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2b25-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="b2b25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2b25-110">EXAMPLES</span></span>

### <span data-ttu-id="b2b25-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2b25-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b2b25-112">Esse comando desabilita a segurança avançada de dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b2b25-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b2b25-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2b25-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="b2b25-114">Esse comando desabilita a segurança avançada de dados no espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2b25-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b2b25-115">OS</span><span class="sxs-lookup"><span data-stu-id="b2b25-115">PARAMETERS</span></span>

### <span data-ttu-id="b2b25-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2b25-116">-AsJob</span></span>
<span data-ttu-id="b2b25-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2b25-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2b25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b25-118">-DefaultProfile</span></span>
<span data-ttu-id="b2b25-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b25-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b25-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2b25-120">-InputObject</span></span>
<span data-ttu-id="b2b25-121">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2b25-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b25-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2b25-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2b25-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2b25-124">-ResourceId</span></span>
<span data-ttu-id="b2b25-125">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2b25-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b2b25-126">-WorkspaceName</span></span>
<span data-ttu-id="b2b25-127">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2b25-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2b25-128">-Confirm</span></span>
<span data-ttu-id="b2b25-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b25-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b25-130">-WhatIf</span></span>
<span data-ttu-id="b2b25-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2b25-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b25-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2b25-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b25-133">CommonParameters</span></span>
<span data-ttu-id="b2b25-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b25-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b25-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2b25-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b25-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2b25-136">INPUTS</span></span>

### <span data-ttu-id="b2b25-137">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b2b25-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b2b25-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2b25-138">OUTPUTS</span></span>

### <span data-ttu-id="b2b25-139">Microsoft. Azure. Commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b2b25-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b2b25-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2b25-140">NOTES</span></span>

## <span data-ttu-id="b2b25-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2b25-141">RELATED LINKS</span></span>
