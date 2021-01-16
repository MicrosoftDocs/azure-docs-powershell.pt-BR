---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263096"
---
# <span data-ttu-id="497d1-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="497d1-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="497d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="497d1-102">SYNOPSIS</span></span>
<span data-ttu-id="497d1-103">Interrompe uma sessão do Spark Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="497d1-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="497d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="497d1-104">SYNTAX</span></span>

### <span data-ttu-id="497d1-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="497d1-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497d1-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="497d1-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="497d1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="497d1-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="497d1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="497d1-108">DESCRIPTION</span></span>
<span data-ttu-id="497d1-109">O cmdlet **Stop-AzSynapseSparkSession** interrompe uma sessão do Spark analítico do Synapse.</span><span class="sxs-lookup"><span data-stu-id="497d1-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="497d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="497d1-110">EXAMPLES</span></span>

### <span data-ttu-id="497d1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="497d1-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="497d1-112">Esse comando interrompe uma sessão do Spark analítico do Synapse.</span><span class="sxs-lookup"><span data-stu-id="497d1-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="497d1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="497d1-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="497d1-114">Esse comando interrompe uma sessão do Spark do Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="497d1-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="497d1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="497d1-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="497d1-116">Esse comando interrompe uma sessão do Spark do Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="497d1-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="497d1-117">OS</span><span class="sxs-lookup"><span data-stu-id="497d1-117">PARAMETERS</span></span>

### <span data-ttu-id="497d1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="497d1-118">-AsJob</span></span>
<span data-ttu-id="497d1-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="497d1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="497d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="497d1-120">-DefaultProfile</span></span>
<span data-ttu-id="497d1-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="497d1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="497d1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="497d1-122">-InputObject</span></span>
<span data-ttu-id="497d1-123">Objeto de entrada de sessão do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="497d1-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497d1-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="497d1-124">-LivyId</span></span>
<span data-ttu-id="497d1-125">Identificador da sessão do Spark.</span><span class="sxs-lookup"><span data-stu-id="497d1-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497d1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="497d1-126">-PassThru</span></span>
<span data-ttu-id="497d1-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="497d1-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="497d1-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="497d1-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="497d1-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="497d1-129">-SparkPoolName</span></span>
<span data-ttu-id="497d1-130">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="497d1-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497d1-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="497d1-131">-SparkPoolObject</span></span>
<span data-ttu-id="497d1-132">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="497d1-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="497d1-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="497d1-133">-WorkspaceName</span></span>
<span data-ttu-id="497d1-134">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="497d1-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497d1-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="497d1-135">-Confirm</span></span>
<span data-ttu-id="497d1-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="497d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="497d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="497d1-137">-WhatIf</span></span>
<span data-ttu-id="497d1-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="497d1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="497d1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="497d1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="497d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497d1-140">CommonParameters</span></span>
<span data-ttu-id="497d1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497d1-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="497d1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497d1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="497d1-143">INPUTS</span></span>

### <span data-ttu-id="497d1-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="497d1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="497d1-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="497d1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="497d1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="497d1-146">OUTPUTS</span></span>

### <span data-ttu-id="497d1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="497d1-147">System.Boolean</span></span>

## <span data-ttu-id="497d1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="497d1-148">NOTES</span></span>

## <span data-ttu-id="497d1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="497d1-149">RELATED LINKS</span></span>
