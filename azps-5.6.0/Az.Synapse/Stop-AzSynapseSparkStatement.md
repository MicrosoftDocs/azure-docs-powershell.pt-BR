---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: a14079c92a59864b98dd086d8e65a340e2a277d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890517"
---
# <span data-ttu-id="f31f0-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="f31f0-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="f31f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f31f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f31f0-103">Cancela uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f31f0-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f31f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f31f0-104">SYNTAX</span></span>

### <span data-ttu-id="f31f0-105">StopSparkStatementByIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f31f0-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f31f0-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f31f0-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f31f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f31f0-107">DESCRIPTION</span></span>
<span data-ttu-id="f31f0-108">O cmdlet **Stop-AzSynapseSparkStatement** cancela uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="f31f0-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="f31f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f31f0-109">EXAMPLES</span></span>

### <span data-ttu-id="f31f0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f31f0-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="f31f0-111">Este comando cancela a instrução Spark com a ID de viol especificada.</span><span class="sxs-lookup"><span data-stu-id="f31f0-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="f31f0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f31f0-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="f31f0-113">Este comando cancela a instrução Spark com a ID de violidade especificada através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="f31f0-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="f31f0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f31f0-114">PARAMETERS</span></span>

### <span data-ttu-id="f31f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31f0-115">-DefaultProfile</span></span>
<span data-ttu-id="f31f0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f31f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31f0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f31f0-117">-Force</span></span>
<span data-ttu-id="f31f0-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f31f0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f31f0-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="f31f0-119">-LivyId</span></span>
<span data-ttu-id="f31f0-120">Identificador da instrução Spark.</span><span class="sxs-lookup"><span data-stu-id="f31f0-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31f0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f31f0-121">-PassThru</span></span>
<span data-ttu-id="f31f0-122">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f31f0-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f31f0-123">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="f31f0-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f31f0-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="f31f0-124">-SessionId</span></span>
<span data-ttu-id="f31f0-125">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="f31f0-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31f0-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="f31f0-126">-SessionObject</span></span>
<span data-ttu-id="f31f0-127">Objeto de entrada de sessão spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f31f0-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f31f0-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f31f0-128">-SparkPoolName</span></span>
<span data-ttu-id="f31f0-129">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="f31f0-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31f0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f31f0-130">-WorkspaceName</span></span>
<span data-ttu-id="f31f0-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f31f0-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f31f0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f31f0-132">-Confirm</span></span>
<span data-ttu-id="f31f0-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f31f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f31f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f31f0-134">-WhatIf</span></span>
<span data-ttu-id="f31f0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f31f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f31f0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f31f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f31f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31f0-137">CommonParameters</span></span>
<span data-ttu-id="f31f0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31f0-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f31f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31f0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f31f0-140">INPUTS</span></span>

### <span data-ttu-id="f31f0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f31f0-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f31f0-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f31f0-142">OUTPUTS</span></span>

### <span data-ttu-id="f31f0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f31f0-143">System.Boolean</span></span>

## <span data-ttu-id="f31f0-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="f31f0-144">NOTES</span></span>

## <span data-ttu-id="f31f0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f31f0-145">RELATED LINKS</span></span>
