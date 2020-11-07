---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947475"
---
# <span data-ttu-id="c19f6-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c19f6-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c19f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c19f6-102">SYNOPSIS</span></span>
<span data-ttu-id="c19f6-103">Invoca uma instrução do Synapse Analytics Analytics.</span><span class="sxs-lookup"><span data-stu-id="c19f6-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c19f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c19f6-104">SYNTAX</span></span>

### <span data-ttu-id="c19f6-105">RunSparkStatementByCodePathParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c19f6-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f6-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19f6-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19f6-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19f6-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19f6-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19f6-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c19f6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c19f6-109">DESCRIPTION</span></span>
<span data-ttu-id="c19f6-110">O cmdlet **Invoke-AzSynapseSparkStatement** invoca uma declaração do Synapse analítico do.</span><span class="sxs-lookup"><span data-stu-id="c19f6-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c19f6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c19f6-111">EXAMPLES</span></span>

### <span data-ttu-id="c19f6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c19f6-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="c19f6-113">Esses comandos iniciam uma sessão do Spark e invocam uma instrução do Spark embutida por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="c19f6-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="c19f6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c19f6-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="c19f6-115">Esses comandos iniciam uma sessão do Spark e invocam uma instrução do Spark embutida.</span><span class="sxs-lookup"><span data-stu-id="c19f6-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="c19f6-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c19f6-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="c19f6-117">Esses comandos iniciam uma sessão do Spark e invocam as instruções do Spark em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c19f6-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="c19f6-118">OS</span><span class="sxs-lookup"><span data-stu-id="c19f6-118">PARAMETERS</span></span>

### <span data-ttu-id="c19f6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c19f6-119">-AsJob</span></span>
<span data-ttu-id="c19f6-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c19f6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c19f6-121">-Código</span><span class="sxs-lookup"><span data-stu-id="c19f6-121">-Code</span></span>
<span data-ttu-id="c19f6-122">O código de execução.</span><span class="sxs-lookup"><span data-stu-id="c19f6-122">The execution code.</span></span>

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

### <span data-ttu-id="c19f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19f6-123">-DefaultProfile</span></span>
<span data-ttu-id="c19f6-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c19f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19f6-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c19f6-125">-FilePath</span></span>
<span data-ttu-id="c19f6-126">Especifica um caminho de arquivo local que contém o código de execução.</span><span class="sxs-lookup"><span data-stu-id="c19f6-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="c19f6-127">-Idioma</span><span class="sxs-lookup"><span data-stu-id="c19f6-127">-Language</span></span>
<span data-ttu-id="c19f6-128">Idioma do código de execução.</span><span class="sxs-lookup"><span data-stu-id="c19f6-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="c19f6-129">-Resposta</span><span class="sxs-lookup"><span data-stu-id="c19f6-129">-Response</span></span>
<span data-ttu-id="c19f6-130">Indica que a resposta completa deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="c19f6-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="c19f6-131">-Identificação_da_sessão</span><span class="sxs-lookup"><span data-stu-id="c19f6-131">-SessionId</span></span>
<span data-ttu-id="c19f6-132">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="c19f6-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="c19f6-133">-Sessionobject</span><span class="sxs-lookup"><span data-stu-id="c19f6-133">-SessionObject</span></span>
<span data-ttu-id="c19f6-134">Objeto de entrada de sessão do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c19f6-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c19f6-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c19f6-135">-SparkPoolName</span></span>
<span data-ttu-id="c19f6-136">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="c19f6-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c19f6-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c19f6-137">-WorkspaceName</span></span>
<span data-ttu-id="c19f6-138">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="c19f6-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c19f6-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c19f6-139">-Confirm</span></span>
<span data-ttu-id="c19f6-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c19f6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19f6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19f6-141">-WhatIf</span></span>
<span data-ttu-id="c19f6-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c19f6-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c19f6-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c19f6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19f6-144">CommonParameters</span></span>
<span data-ttu-id="c19f6-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19f6-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c19f6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19f6-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c19f6-147">INPUTS</span></span>

### <span data-ttu-id="c19f6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c19f6-148">System.String</span></span>

### <span data-ttu-id="c19f6-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c19f6-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c19f6-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c19f6-150">OUTPUTS</span></span>

### <span data-ttu-id="c19f6-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c19f6-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="c19f6-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c19f6-152">NOTES</span></span>

## <span data-ttu-id="c19f6-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c19f6-153">RELATED LINKS</span></span>
