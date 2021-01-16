---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262129"
---
# <span data-ttu-id="0d1c2-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d1c2-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="0d1c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1c2-103">Cria um banco de dados SQL analítico do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0d1c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d1c2-104">SYNTAX</span></span>

### <span data-ttu-id="0d1c2-105">CreateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d1c2-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c2-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d1c2-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1c2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="0d1c2-108">O cmdlet **Get-AzSynapseSqlDatabase** Obtém informações sobre um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0d1c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="0d1c2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d1c2-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="0d1c2-111">Esse comando cria um banco de dados SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="0d1c2-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d1c2-112">PARAMETERS</span></span>

### <span data-ttu-id="0d1c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d1c2-113">-AsJob</span></span>
<span data-ttu-id="0d1c2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0d1c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d1c2-115">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="0d1c2-115">-Collation</span></span>
<span data-ttu-id="0d1c2-116">O agrupamento define as regras que classificam e comparam dados, e não podem ser alterados após a criação do pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="0d1c2-117">O agrupamento padrão é SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="0d1c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1c2-118">-DefaultProfile</span></span>
<span data-ttu-id="0d1c2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1c2-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="0d1c2-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="0d1c2-121">Especifica o tamanho máximo do banco de dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d1c2-122">-Name</span></span>
<span data-ttu-id="0d1c2-123">Nome do banco de dados SQL do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="0d1c2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1c2-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d1c2-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c2-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="0d1c2-126">-Tag</span></span>
<span data-ttu-id="0d1c2-127">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0d1c2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d1c2-128">-WorkspaceName</span></span>
<span data-ttu-id="0d1c2-129">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c2-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0d1c2-130">-WorkspaceObject</span></span>
<span data-ttu-id="0d1c2-131">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c2-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d1c2-132">-Confirm</span></span>
<span data-ttu-id="0d1c2-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1c2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1c2-134">-WhatIf</span></span>
<span data-ttu-id="0d1c2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1c2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1c2-137">CommonParameters</span></span>
<span data-ttu-id="0d1c2-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1c2-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d1c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1c2-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d1c2-140">INPUTS</span></span>

### <span data-ttu-id="0d1c2-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d1c2-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0d1c2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d1c2-142">OUTPUTS</span></span>

### <span data-ttu-id="0d1c2-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d1c2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="0d1c2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d1c2-144">NOTES</span></span>

## <span data-ttu-id="0d1c2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d1c2-145">RELATED LINKS</span></span>
