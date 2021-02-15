---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113913"
---
# <span data-ttu-id="0b3ef-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="0b3ef-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="0b3ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3ef-103">Vincula um armazenamento de dados ou um serviço de nuvem ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="0b3ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b3ef-104">SYNTAX</span></span>

### <span data-ttu-id="0b3ef-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b3ef-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3ef-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="0b3ef-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3ef-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b3ef-107">DESCRIPTION</span></span>
<span data-ttu-id="0b3ef-108">O **cmdlet Set-AzSynapseLinkedService** vincula um armazenamento de dados ou um serviço de nuvem ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="0b3ef-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b3ef-109">EXAMPLES</span></span>

### <span data-ttu-id="0b3ef-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b3ef-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="0b3ef-111">Esse comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0b3ef-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0b3ef-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="0b3ef-113">Esse comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0b3ef-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b3ef-114">PARAMETERS</span></span>

### <span data-ttu-id="0b3ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b3ef-115">-AsJob</span></span>
<span data-ttu-id="0b3ef-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0b3ef-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b3ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3ef-117">-DefaultProfile</span></span>
<span data-ttu-id="0b3ef-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3ef-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0b3ef-119">-DefinitionFile</span></span>
<span data-ttu-id="0b3ef-120">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ef-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b3ef-121">-Name</span></span>
<span data-ttu-id="0b3ef-122">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ef-123">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="0b3ef-123">-WorkspaceName</span></span>
<span data-ttu-id="0b3ef-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ef-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b3ef-125">-WorkspaceObject</span></span>
<span data-ttu-id="0b3ef-126">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3ef-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0b3ef-127">-Confirm</span></span>
<span data-ttu-id="0b3ef-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3ef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3ef-129">-WhatIf</span></span>
<span data-ttu-id="0b3ef-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b3ef-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3ef-132">CommonParameters</span></span>
<span data-ttu-id="0b3ef-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3ef-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b3ef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3ef-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b3ef-135">INPUTS</span></span>

### <span data-ttu-id="0b3ef-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b3ef-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0b3ef-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b3ef-137">OUTPUTS</span></span>

### <span data-ttu-id="0b3ef-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="0b3ef-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0b3ef-139">Notas</span><span class="sxs-lookup"><span data-stu-id="0b3ef-139">NOTES</span></span>

## <span data-ttu-id="0b3ef-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b3ef-140">RELATED LINKS</span></span>
