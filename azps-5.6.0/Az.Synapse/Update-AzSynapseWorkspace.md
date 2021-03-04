---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 60631b8d4c42ac314268453c5dedf16893281861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891072"
---
# <span data-ttu-id="28af6-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="28af6-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="28af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28af6-102">SYNOPSIS</span></span>
<span data-ttu-id="28af6-103">Atualiza um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="28af6-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="28af6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28af6-104">SYNTAX</span></span>

### <span data-ttu-id="28af6-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28af6-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28af6-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28af6-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28af6-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28af6-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28af6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28af6-108">DESCRIPTION</span></span>
<span data-ttu-id="28af6-109">O cmdlet **Update-AzSynapseWorkspace** atualiza um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="28af6-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="28af6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28af6-110">EXAMPLES</span></span>

### <span data-ttu-id="28af6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28af6-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="28af6-112">Esse comandos atualiza marcas para o espaço de trabalho especificado do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="28af6-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="28af6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28af6-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="28af6-114">Este comandos atualiza marcas para o espaço de trabalho do Azure Synapse Analytics especificado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="28af6-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="28af6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="28af6-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="28af6-116">Esse comandos atualiza marcas para o espaço de trabalho do Azure Synapse Analytics especificado por meio de pipeline com iD de recurso.</span><span class="sxs-lookup"><span data-stu-id="28af6-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="28af6-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28af6-117">PARAMETERS</span></span>

### <span data-ttu-id="28af6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28af6-118">-AsJob</span></span>
<span data-ttu-id="28af6-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28af6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28af6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28af6-120">-DefaultProfile</span></span>
<span data-ttu-id="28af6-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28af6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28af6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28af6-122">-InputObject</span></span>
<span data-ttu-id="28af6-123">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="28af6-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="28af6-124">-Name</span></span>
<span data-ttu-id="28af6-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="28af6-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28af6-126">-ResourceGroupName</span></span>
<span data-ttu-id="28af6-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28af6-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28af6-128">-ResourceId</span></span>
<span data-ttu-id="28af6-129">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="28af6-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="28af6-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="28af6-131">A nova SQL de administrador para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="28af6-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="28af6-132">-Tag</span></span>
<span data-ttu-id="28af6-133">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="28af6-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28af6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28af6-134">-Confirm</span></span>
<span data-ttu-id="28af6-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28af6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28af6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28af6-136">-WhatIf</span></span>
<span data-ttu-id="28af6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28af6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28af6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28af6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28af6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28af6-139">CommonParameters</span></span>
<span data-ttu-id="28af6-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28af6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28af6-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28af6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28af6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28af6-142">INPUTS</span></span>

### <span data-ttu-id="28af6-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="28af6-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="28af6-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28af6-144">OUTPUTS</span></span>

### <span data-ttu-id="28af6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="28af6-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="28af6-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="28af6-146">NOTES</span></span>

## <span data-ttu-id="28af6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28af6-147">RELATED LINKS</span></span>
