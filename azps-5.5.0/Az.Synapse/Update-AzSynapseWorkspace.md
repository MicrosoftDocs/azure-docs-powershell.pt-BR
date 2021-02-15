---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116299"
---
# <span data-ttu-id="b94d5-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b94d5-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="b94d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b94d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b94d5-103">Atualiza um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b94d5-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b94d5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b94d5-104">SYNTAX</span></span>

### <span data-ttu-id="b94d5-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b94d5-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b94d5-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b94d5-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b94d5-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b94d5-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b94d5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b94d5-108">DESCRIPTION</span></span>
<span data-ttu-id="b94d5-109">O cmdlet **Update-AzSynapseWorkspace** atualiza um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b94d5-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="b94d5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b94d5-110">EXAMPLES</span></span>

### <span data-ttu-id="b94d5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b94d5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="b94d5-112">Esse comando atualiza marcas para o espaço de trabalho especificado do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b94d5-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="b94d5-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b94d5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="b94d5-114">Esse comando atualiza marcas para o espaço de trabalho especificado do Azure Synapse Analytics por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b94d5-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="b94d5-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b94d5-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="b94d5-116">Esse comando atualiza marcas para o espaço de trabalho especificado do Azure Synapse Analytics por meio de pipeline com ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="b94d5-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="b94d5-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b94d5-117">PARAMETERS</span></span>

### <span data-ttu-id="b94d5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b94d5-118">-AsJob</span></span>
<span data-ttu-id="b94d5-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b94d5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b94d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94d5-120">-DefaultProfile</span></span>
<span data-ttu-id="b94d5-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b94d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b94d5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b94d5-122">-InputObject</span></span>
<span data-ttu-id="b94d5-123">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b94d5-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b94d5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b94d5-124">-Name</span></span>
<span data-ttu-id="b94d5-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b94d5-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b94d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b94d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="b94d5-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b94d5-127">Resource group name.</span></span>

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

### <span data-ttu-id="b94d5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b94d5-128">-ResourceId</span></span>
<span data-ttu-id="b94d5-129">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b94d5-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="b94d5-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b94d5-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="b94d5-131">A nova senha de administrador sql do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b94d5-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="b94d5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b94d5-132">-Tag</span></span>
<span data-ttu-id="b94d5-133">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="b94d5-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="b94d5-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b94d5-134">-Confirm</span></span>
<span data-ttu-id="b94d5-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b94d5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b94d5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b94d5-136">-WhatIf</span></span>
<span data-ttu-id="b94d5-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b94d5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b94d5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b94d5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b94d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94d5-139">CommonParameters</span></span>
<span data-ttu-id="b94d5-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94d5-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b94d5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94d5-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="b94d5-142">INPUTS</span></span>

### <span data-ttu-id="b94d5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b94d5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b94d5-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="b94d5-144">OUTPUTS</span></span>

### <span data-ttu-id="b94d5-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b94d5-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b94d5-146">Notas</span><span class="sxs-lookup"><span data-stu-id="b94d5-146">NOTES</span></span>

## <span data-ttu-id="b94d5-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b94d5-147">RELATED LINKS</span></span>
