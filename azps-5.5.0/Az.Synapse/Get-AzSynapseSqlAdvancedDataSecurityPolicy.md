---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116316"
---
# <span data-ttu-id="8d5fb-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5fb-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="8d5fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5fb-103">Obtém uma política de Segurança de Dados Avançada de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="8d5fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d5fb-104">SYNTAX</span></span>

### <span data-ttu-id="8d5fb-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d5fb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5fb-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5fb-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5fb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d5fb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5fb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d5fb-108">DESCRIPTION</span></span>
<span data-ttu-id="8d5fb-109">O cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** recupera a política de Segurança de Dados Avançada de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="8d5fb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d5fb-110">EXAMPLES</span></span>

### <span data-ttu-id="8d5fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d5fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8d5fb-112">Esse comando obtém a Segurança de Dados Avançada no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8d5fb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8d5fb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="8d5fb-114">Esse comando obtém a Segurança de Dados Avançada no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8d5fb-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d5fb-115">PARAMETERS</span></span>

### <span data-ttu-id="8d5fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5fb-116">-DefaultProfile</span></span>
<span data-ttu-id="8d5fb-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d5fb-118">-InputObject</span></span>
<span data-ttu-id="8d5fb-119">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5fb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5fb-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d5fb-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-121">Resource group name.</span></span>

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

### <span data-ttu-id="8d5fb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5fb-122">-ResourceId</span></span>
<span data-ttu-id="8d5fb-123">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="8d5fb-124">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8d5fb-124">-WorkspaceName</span></span>
<span data-ttu-id="8d5fb-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8d5fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5fb-126">CommonParameters</span></span>
<span data-ttu-id="8d5fb-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5fb-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d5fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5fb-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="8d5fb-129">INPUTS</span></span>

### <span data-ttu-id="8d5fb-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d5fb-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8d5fb-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="8d5fb-131">OUTPUTS</span></span>

### <span data-ttu-id="8d5fb-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="8d5fb-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="8d5fb-133">Notas</span><span class="sxs-lookup"><span data-stu-id="8d5fb-133">NOTES</span></span>

## <span data-ttu-id="8d5fb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d5fb-134">RELATED LINKS</span></span>
