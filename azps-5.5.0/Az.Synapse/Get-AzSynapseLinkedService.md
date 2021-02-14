---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116063"
---
# <span data-ttu-id="27836-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="27836-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="27836-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27836-102">SYNOPSIS</span></span>
<span data-ttu-id="27836-103">Obtém informações sobre serviços vinculados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="27836-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="27836-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27836-104">SYNTAX</span></span>

### <span data-ttu-id="27836-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="27836-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27836-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="27836-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27836-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="27836-107">DESCRIPTION</span></span>
<span data-ttu-id="27836-108">O cmdlet **Get-AzSynapseLinkedService** obtém informações sobre serviços vinculados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="27836-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="27836-109">Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="27836-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="27836-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os serviços vinculados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="27836-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="27836-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27836-111">EXAMPLES</span></span>

### <span data-ttu-id="27836-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="27836-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="27836-113">Esse comando obtém informações sobre todos os serviços vinculados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="27836-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="27836-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="27836-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="27836-115">Esse comando obtém informações sobre o serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="27836-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="27836-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="27836-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="27836-117">Esse comando obtém informações sobre o serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="27836-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="27836-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27836-118">PARAMETERS</span></span>

### <span data-ttu-id="27836-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27836-119">-DefaultProfile</span></span>
<span data-ttu-id="27836-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27836-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27836-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="27836-121">-Name</span></span>
<span data-ttu-id="27836-122">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="27836-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27836-123">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="27836-123">-WorkspaceName</span></span>
<span data-ttu-id="27836-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="27836-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27836-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="27836-125">-WorkspaceObject</span></span>
<span data-ttu-id="27836-126">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="27836-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27836-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27836-127">CommonParameters</span></span>
<span data-ttu-id="27836-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27836-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27836-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27836-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27836-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="27836-130">INPUTS</span></span>

### <span data-ttu-id="27836-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27836-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="27836-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="27836-132">OUTPUTS</span></span>

### <span data-ttu-id="27836-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="27836-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="27836-134">Notas</span><span class="sxs-lookup"><span data-stu-id="27836-134">NOTES</span></span>

## <span data-ttu-id="27836-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27836-135">RELATED LINKS</span></span>
