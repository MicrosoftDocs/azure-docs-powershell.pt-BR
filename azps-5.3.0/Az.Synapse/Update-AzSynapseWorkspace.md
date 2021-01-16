---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271996"
---
# <span data-ttu-id="3fd3f-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fd3f-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="3fd3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd3f-103">Atualiza um espaço de trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3fd3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fd3f-104">SYNTAX</span></span>

### <span data-ttu-id="3fd3f-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3fd3f-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd3f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd3f-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd3f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd3f-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fd3f-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd3f-109">O cmdlet **Update-AzSynapseWorkspace** atualiza um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3fd3f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fd3f-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd3f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3fd3f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="3fd3f-112">Esses comandos atualizam as marcas do espaço de trabalho de análise do Azure Synapse specififed.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="3fd3f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3fd3f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="3fd3f-114">Esses comandos atualizam as marcas do espaço de trabalho de análise do Azure Synapse do specififed por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="3fd3f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3fd3f-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="3fd3f-116">Esses comandos atualizam as marcas do espaço de trabalho de análise do Azure Synapse do specififed por meio do pipeline com a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="3fd3f-117">OS</span><span class="sxs-lookup"><span data-stu-id="3fd3f-117">PARAMETERS</span></span>

### <span data-ttu-id="3fd3f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fd3f-118">-AsJob</span></span>
<span data-ttu-id="3fd3f-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3fd3f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fd3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd3f-120">-DefaultProfile</span></span>
<span data-ttu-id="3fd3f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd3f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fd3f-122">-InputObject</span></span>
<span data-ttu-id="3fd3f-123">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fd3f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fd3f-124">-Name</span></span>
<span data-ttu-id="3fd3f-125">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fd3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fd3f-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-127">Resource group name.</span></span>

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

### <span data-ttu-id="3fd3f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd3f-128">-ResourceId</span></span>
<span data-ttu-id="3fd3f-129">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fd3f-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3fd3f-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="3fd3f-131">A nova senha de administrador do SQL para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="3fd3f-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="3fd3f-132">-Tag</span></span>
<span data-ttu-id="3fd3f-133">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="3fd3f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fd3f-134">-Confirm</span></span>
<span data-ttu-id="3fd3f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd3f-136">-WhatIf</span></span>
<span data-ttu-id="3fd3f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd3f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd3f-139">CommonParameters</span></span>
<span data-ttu-id="3fd3f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd3f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fd3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd3f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fd3f-142">INPUTS</span></span>

### <span data-ttu-id="3fd3f-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fd3f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3fd3f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fd3f-144">OUTPUTS</span></span>

### <span data-ttu-id="3fd3f-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fd3f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3fd3f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fd3f-146">NOTES</span></span>

## <span data-ttu-id="3fd3f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fd3f-147">RELATED LINKS</span></span>
