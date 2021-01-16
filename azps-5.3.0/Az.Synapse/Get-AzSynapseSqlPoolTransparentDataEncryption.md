---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272406"
---
# <span data-ttu-id="2b650-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="2b650-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="2b650-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b650-102">SYNOPSIS</span></span>
<span data-ttu-id="2b650-103">Obtém o estado TDE de um pool SQL.</span><span class="sxs-lookup"><span data-stu-id="2b650-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="2b650-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b650-104">SYNTAX</span></span>

### <span data-ttu-id="2b650-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b650-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b650-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b650-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b650-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b650-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b650-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b650-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b650-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b650-109">DESCRIPTION</span></span>
<span data-ttu-id="2b650-110">O cmdlet **Get-AzSynapseSqlPoolTransparentDataEncryption** Obtém o estado de criptografia de dados transparente (TDE) para um pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2b650-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2b650-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b650-111">EXAMPLES</span></span>

### <span data-ttu-id="2b650-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b650-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2b650-113">Esse comando obtém o status de TDE para o pool SQL chamado ContosoSqlPool sob o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2b650-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2b650-114">OS</span><span class="sxs-lookup"><span data-stu-id="2b650-114">PARAMETERS</span></span>

### <span data-ttu-id="2b650-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b650-115">-DefaultProfile</span></span>
<span data-ttu-id="2b650-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b650-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b650-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b650-117">-InputObject</span></span>
<span data-ttu-id="2b650-118">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b650-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b650-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b650-119">-Name</span></span>
<span data-ttu-id="2b650-120">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b650-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b650-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b650-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b650-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b650-122">Resource group name.</span></span>

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

### <span data-ttu-id="2b650-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b650-123">-ResourceId</span></span>
<span data-ttu-id="2b650-124">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b650-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="2b650-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b650-125">-WorkspaceName</span></span>
<span data-ttu-id="2b650-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2b650-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2b650-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2b650-127">-WorkspaceObject</span></span>
<span data-ttu-id="2b650-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b650-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2b650-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b650-129">CommonParameters</span></span>
<span data-ttu-id="2b650-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b650-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b650-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b650-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b650-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b650-132">INPUTS</span></span>

### <span data-ttu-id="2b650-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b650-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2b650-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2b650-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2b650-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b650-135">OUTPUTS</span></span>

### <span data-ttu-id="2b650-136">Microsoft. Azure. Commands. Synapse. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="2b650-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="2b650-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b650-137">NOTES</span></span>

## <span data-ttu-id="2b650-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b650-138">RELATED LINKS</span></span>
