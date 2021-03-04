---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 62894b5d879febdeeb7c14360c16c66fb8a28ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889381"
---
# <span data-ttu-id="dc85b-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="dc85b-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="dc85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc85b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc85b-103">Invoca uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dc85b-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="dc85b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc85b-104">SYNTAX</span></span>

### <span data-ttu-id="dc85b-105">RunSparkStatementByCodePathParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc85b-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc85b-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc85b-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc85b-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc85b-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc85b-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc85b-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc85b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc85b-109">DESCRIPTION</span></span>
<span data-ttu-id="dc85b-110">O cmdlet **Invoke-AzSynapseSparkStatement** invoca uma instrução Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dc85b-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="dc85b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc85b-111">EXAMPLES</span></span>

### <span data-ttu-id="dc85b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc85b-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="dc85b-113">Esses comandos iniciam uma sessão Spark e invocam uma instrução Spark em linha por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc85b-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="dc85b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dc85b-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="dc85b-115">Esses comandos iniciam uma sessão Spark e invocam uma instrução Spark em linha.</span><span class="sxs-lookup"><span data-stu-id="dc85b-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="dc85b-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dc85b-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="dc85b-117">Esses comandos iniciam uma sessão Spark e invocam instruções Spark em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dc85b-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="dc85b-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc85b-118">PARAMETERS</span></span>

### <span data-ttu-id="dc85b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc85b-119">-AsJob</span></span>
<span data-ttu-id="dc85b-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dc85b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc85b-121">-Code</span><span class="sxs-lookup"><span data-stu-id="dc85b-121">-Code</span></span>
<span data-ttu-id="dc85b-122">O código de execução.</span><span class="sxs-lookup"><span data-stu-id="dc85b-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc85b-123">-DefaultProfile</span></span>
<span data-ttu-id="dc85b-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc85b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc85b-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="dc85b-125">-FilePath</span></span>
<span data-ttu-id="dc85b-126">Especifica um caminho de arquivo local que contém o código de execução.</span><span class="sxs-lookup"><span data-stu-id="dc85b-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-127">-Language</span><span class="sxs-lookup"><span data-stu-id="dc85b-127">-Language</span></span>
<span data-ttu-id="dc85b-128">Idioma do código de execução.</span><span class="sxs-lookup"><span data-stu-id="dc85b-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-129">-Response</span><span class="sxs-lookup"><span data-stu-id="dc85b-129">-Response</span></span>
<span data-ttu-id="dc85b-130">Indica que a resposta completa deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="dc85b-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="dc85b-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="dc85b-131">-SessionId</span></span>
<span data-ttu-id="dc85b-132">Identificador da sessão Spark.</span><span class="sxs-lookup"><span data-stu-id="dc85b-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="dc85b-133">-SessionObject</span></span>
<span data-ttu-id="dc85b-134">Objeto de entrada de sessão spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc85b-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="dc85b-135">-SparkPoolName</span></span>
<span data-ttu-id="dc85b-136">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="dc85b-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc85b-137">-WorkspaceName</span></span>
<span data-ttu-id="dc85b-138">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc85b-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc85b-139">-Confirm</span></span>
<span data-ttu-id="dc85b-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc85b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc85b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc85b-141">-WhatIf</span></span>
<span data-ttu-id="dc85b-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc85b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc85b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc85b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc85b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc85b-144">CommonParameters</span></span>
<span data-ttu-id="dc85b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc85b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc85b-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc85b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc85b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc85b-147">INPUTS</span></span>

### <span data-ttu-id="dc85b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="dc85b-148">System.String</span></span>

### <span data-ttu-id="dc85b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="dc85b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="dc85b-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc85b-150">OUTPUTS</span></span>

### <span data-ttu-id="dc85b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="dc85b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="dc85b-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc85b-152">NOTES</span></span>

## <span data-ttu-id="dc85b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc85b-153">RELATED LINKS</span></span>
